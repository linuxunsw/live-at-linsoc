<script>
  import Lal4 from './lal4.jpg';
</script>

<div>
  <img alt="" src={Lal4} />
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
    bottom: calc(0px - var(--scroll) * 2.5px);
    opacity: calc(300 / var(--scroll));
    right: 0;
    position: fixed;
    min-width: 100vw;
    object-fit: cover;
    z-index: -10;
  }
</style>
