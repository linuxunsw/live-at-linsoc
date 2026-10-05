<script lang="ts">
  import { MediaQuery } from 'svelte/reactivity';
  import Credits from './Credits.svelte';

  const { children } = $props();

  const reducedMotion = new MediaQuery('prefers-reduced-motion: reduce');

  // Adapted from: https://www.joshwcomeau.com/snippets/javascript/debounce/
  function debounce<T>(callback: (...a: T[]) => void, wait: number): (...a: T[]) => void {
    let timeoutId: ReturnType<typeof setTimeout> | null = null;
    return (...args) => {
      if (timeoutId) {
        clearTimeout(timeoutId);
      }
      timeoutId = setTimeout(() => {
        callback(...args);
      }, wait);
    };
  };

  const storeScrollPosition = () => {
    document.documentElement.style.setProperty('--scroll', `${document.documentElement.scrollTop}`);
    document.documentElement.style.setProperty(
      '--scroll-reduced-motion',
      reducedMotion.current ? '0' : `${document.documentElement.scrollTop}`,
    );
  };

  $effect(debounce(storeScrollPosition, 250));
</script>

<svelte:window onscroll={storeScrollPosition} onresize={storeScrollPosition} />

{@render children()}

<Credits />
