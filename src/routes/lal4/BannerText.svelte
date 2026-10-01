<h1>
  <span class="live">LIVE</span>
  <span class="at">@</span>
  <span class="linsoc">LNSC</span>
</h1>

<style>
  h1 {
    display: flex;
    flex-direction: column;
    align-items: center;
    font-family: monospace;
    font-size: calc(min(28vw, 20vh, 15rem));
    letter-spacing: 10px;
    margin: 0;
    margin-top: 10vh;
    text-shadow: 0px 0px 5px white;
  }

  .live {
    transform: rotate(calc(1.5deg - var(--scroll-reduced-motion) * 0.02deg));
    height: calc(min(30vw, 20vh, 15rem) * 0.6);
  }
  .at {
    transform: rotate(calc(-1deg - var(--scroll-reduced-motion) * 0.02deg))
      scale(calc(1.25 + var(--scroll-reduced-motion) * 0.0004));
    height: calc(min(30vw, 20vh, 15rem) * 0.9);
    z-index: 1;
  }
  .linsoc {
    transform: rotate(calc(-2.5deg + var(--scroll-reduced-motion) * 0.02deg));
  }
</style>
