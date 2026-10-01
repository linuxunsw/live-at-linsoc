<script>
  import Aaryan from './26t3w4/Aaryan.svelte';
  import Background from './26t3w4/Background.svelte';
  import Hero from './26t3w4/Hero.svelte';
  import Cameron from './26t3w4/Cameron.svelte';
  import Evan from './26t3w4/Evan.svelte';
  import Wiki from './26t3w4/Wiki.svelte';
</script>

<Background />

<div id="hero">
  <Hero />
</div>

<main id="main">
  <p class="event-description">
    Join us for 2 hours of student-run presentations, exploring the world of software engineering,
    including topics on free and open-source software, Linux, security, self-hosting, and programming.
  </p>

  <h2>26T3 Line-up</h2>

  <Wiki />
  <Cameron />
  <Evan />
  <Aaryan />
</main>

<style>
  :root {
    font-family: Charter, 'Bitstream Charter', 'Sitka Text', Cambria, serif;
    font-weight: normal;
  }
  #hero {
    height: 90vh;
  }

  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 20px;
    color: white;
    font-size: 1.3rem;
  }

  .event-description {
    text-align: center;
    max-width: 800px;
    transform: rotate(calc(-1deg + var(--scroll-reduced-motion) * 0.001deg));
  }

  h2 {
    font-size: 3.5rem;
    transform: rotate(calc(1deg + var(--scroll-reduced-motion) * 0.002deg));
  }
</style>
