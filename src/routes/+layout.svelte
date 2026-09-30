<script lang="ts">
  import favicon from '$lib/assets/favicon.svg';
  import Credits from './Credits.svelte';

  const { children } = $props();

  const storeScrollPosition = () => {
    document.documentElement.style.setProperty('--scroll', `${document.documentElement.scrollTop}`);
  };

  $effect(storeScrollPosition);
</script>

<svelte:window onscroll={storeScrollPosition} onresize={storeScrollPosition} />

<svelte:head>
  <link rel="icon" href={favicon} />
</svelte:head>

{@render children()}

<Credits />
