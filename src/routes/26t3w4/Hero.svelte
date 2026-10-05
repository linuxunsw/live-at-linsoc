<div class="hero">
  <h1>
    <span class="live">LIVE</span>
    <span class="at">@</span>
    <span class="linsoc">LNSC</span>
  </h1>
  <div class="event-info">
    <span class="date">Friday 9th October (Week 4)</span>
    <span class="time">12-2 PM</span>
    <span class="location"><a target="_blank" href="https://link.mazemap.com/ZGwAjS3l"><i class="las la-link"></i>H13 Lawrence Theatre</a></span>
    <span class="tix"><a target="_blank" href="https://campus.hellorubric.com/?eid=85710"><i class="las la-link"></i>Get your tickets</a></span>
    <span class="down">
      <a href="#main" aria-label="Scroll down to content">
        <i class="las la-angle-down"></i>
      </a>
    </span>
  </div>
</div>

<style>
  .hero {
    text-shadow: 0px 0px 5px white;
    color: black;
  }
  h1 {
    display: flex;
    flex-direction: column;
    align-items: center;
    font-family: monospace;
    font-size: calc(min(28vw, 20vh, 15rem));
    letter-spacing: 10px;
    margin: 0;
    margin-top: 10vh;
  }

  .live {
    transform: rotate(calc(1.5deg - var(--scroll-reduced-motion) * 0.02deg));
    transition: all 0.1s linear;
    height: calc(min(30vw, 20vh, 15rem) * 0.6);
  }
  .at {
    transform: rotate(calc(-1deg - var(--scroll-reduced-motion) * 0.02deg))
      scale(calc(1.25 + var(--scroll-reduced-motion) * 0.0004));
    transition: all 0.1s linear;
    height: calc(min(30vw, 20vh, 15rem) * 0.9);
    z-index: 1;
  }
  .linsoc {
    transform: rotate(calc(-2.5deg + var(--scroll-reduced-motion) * 0.02deg));
    transition: all 0.1s linear;
  }

  .event-info {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 5px;
  }
  .date {
    font-size: calc(min(3rem, 6vw, 6vh));
    transform: rotate(calc(2deg - var(--scroll-reduced-motion) * 0.02deg))
      scale(calc(1 - var(--scroll-reduced-motion) * 0.0001));
    transition: all 0.1s linear;
  }
  .time {
    font-size: calc(min(2.5rem, 5vw, 5vh));
    transform: rotate(calc(-3deg + var(--scroll-reduced-motion) * 0.01deg))
      scale(calc(1 + var(--scroll-reduced-motion) * 0.0002));
    transition: all 0.1s linear;
  }
  .location {
    font-size: calc(min(3rem, 6vw, 6vh));
    transform: rotate(calc(1deg + var(--scroll-reduced-motion) * 0.005deg))
      scale(calc(1 + var(--scroll-reduced-motion) * 0.0001));
    transition: all 0.1s linear;
  }
  .tix {
    font-size: calc(min(3.5rem, 7vw, 7vh));
    transform: rotate(calc(-1deg - var(--scroll-reduced-motion) * 0.02deg))
      scale(calc(1 + var(--scroll-reduced-motion) * 0.0003));
    transition: all 0.1s linear;
  }
  a {
    color: black;
    text-decoration: underline dotted;
  }
  a:hover {
    text-decoration: underline;
  }
  .down {
    font-size: 3rem;
    transition: translate 0.2s;
    transition: all 0.1s linear;
  }
  .down:hover {
    translate: 0 5px;
  }

  @media (prefers-contrast: more) {
    .hero {
      text-shadow: none;
      color: white;
    }
    .at {
      transform: scale(70%);
    }
    a {
      color: white;
    }
  }
</style>
