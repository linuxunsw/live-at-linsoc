<script lang="ts">
  type Splotch = {
    id: number,
    color: string,
    x: string,
    y: string,
    timespan: string,
    spread: string,
  };

  const numSplotches = 300;

  const colours = [
    '#ffe196',
    '#ffd300',
    '#ffb643',
    '#a0fbff',
    '#ffe7d7',
    '#fffbea',
  ];

  const splotches: Splotch[] = $derived(
    [...Array(numSplotches).keys()].map((_, i) => ({
      id: i,
      color: colours[Math.floor(Math.random() * colours.length)],
      x: `${Math.random()}`,
      y: `${Math.random()}`,
      timespan: `${Math.random()}`,
      spread: `${Math.random()}`,
    })),
  );
</script>

{#snippet dot(splotch: Splotch)}
  <div
    class="dot"
    style:--color={splotch.color}
    style:--x={splotch.x}
    style:--y={splotch.y}
    style:--duration={splotch.timespan}
    style:--spread={splotch.spread}
  ></div>
{/snippet}
<div class="splotch-box">
  {#each splotches as splotch (splotch.id)}
    {@render dot(splotch)}
  {/each}
</div>
<style>
  .splotch-box {
    opacity: calc(var(--scroll) * 0.5%);
  }

  .dot {
    z-index: -10;
    width: 0;
    height: 0;
    position: absolute;
    left: calc(var(--x) * 100%);
    top: calc(var(--y) * 100%);
    box-shadow: 0 0 calc(var(--spread) * 3px) calc(var(--spread) * 2px) var(--color);
    transition: all 0.5s;
    animation: flicker calc(var(--duration) * 5s + 2s) infinite;
  }

  @keyframes flicker {
    0% {
      opacity: 100%;
    }
    50% {
      opacity: 0%;
    }
    100% {
      opacity: 100%;
    }
  }

  @media (prefers-reduced-motion) {
    .dot {
      transition: all 0s;
    }
  }

  @media (prefers-contrast: more), (prefers-reduced-transparency) {
    .dot {
      box-shadow: none;
    }
  }
</style>
