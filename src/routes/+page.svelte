<script>
  import Aaryan from './lal4/Aaryan.svelte';
  import Background from './lal4/Background.svelte';
  import BannerText from './lal4/BannerText.svelte';
  import Cameron from './lal4/Cameron.svelte';
  import Evan from './lal4/Evan.svelte';
  import EventInfo from './lal4/EventInfo.svelte';
  import Wiki from './lal4/Wiki.svelte';
</script>

<Background />

<div id="hero">
  <BannerText />
  <EventInfo />
</div>

<main>
  <p class="event-description">
    Join us for 2 hours of student-run lightning talks, exploring the world of software engineering,
    including topics on free and open-source software, Linux, security, self-hosting, and programming.
  </p>

  <h2>26T3 Line-up</h2>

  <Wiki />
  <Cameron />
  <Evan />
  <Aaryan />
</main>

<style>
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
  }

  h2 {
    font-size: 3.5rem;
    transform: rotate(calc(1deg + var(--scroll) * 0.002deg));
  }
</style>
