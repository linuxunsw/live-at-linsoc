<script>
  import Lal4 from './lal4.jpg';
  import Stars from './Stars.svelte';
</script>

<div>
  <img alt="" src={Lal4} />

  <Stars />
</div>

<style>
  div {
    position: fixed;
    top: 0;
    width: 100%;
    min-height: 100%;
    background-color: #33148B;
    z-index: -10;
  }
  img {
    bottom: calc(0px - var(--scroll) * 1px);
    opacity: calc(100 / var(--scroll));
    right: 0;
    position: fixed;
    min-width: 100vw;
    object-fit: cover;
    z-index: -9;
  }
</style>
