<script lang="ts">
  import { MediaQuery } from 'svelte/reactivity';
  import favicon from '$lib/assets/favicon.svg';
  import Credits from './Credits.svelte';

  const { children } = $props();

  const reducedMotion = new MediaQuery('prefers-reduced-motion: reduce');

  const storeScrollPosition = () => {
    document.documentElement.style.setProperty('--scroll', `${document.documentElement.scrollTop}`);
    document.documentElement.style.setProperty(
      '--scroll-reduced-motion',
      reducedMotion.current ? '0' : `${document.documentElement.scrollTop}`,
    );
  };

  $effect(storeScrollPosition);
</script>

<svelte:window onscroll={storeScrollPosition} onresize={storeScrollPosition} />

<svelte:head>
  <link rel="icon" href={favicon} />
</svelte:head>

{@render children()}

<Credits />
