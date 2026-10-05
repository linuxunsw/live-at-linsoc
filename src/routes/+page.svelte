<script>
  import Background from './26t3w4/Background.svelte';
  import Hero from './26t3w4/Hero.svelte';
  import Talk from './26t3w4/Talk.svelte';

  const talks = [
    {
      title: 'Initial Userspace and Booting Linux',
      description: 'An overview of what the Linux initial userspace does, covering initrd and initramfs, a couple specialty Linux syscalls and enough extra information to help you feel more confident making your own.',
      presenter: 'Wiki',
    },
    {
      title: 'The Wayland Protocol (Briefly)',
      description: 'A look at the core Wayland Protocol, surfaces and seats, and a discussion of extension Wayland protocols.',
      presenter: 'Cameron',
    },
    {
      title: "ambatuCAM: exploiting cheaters' button cameras",
      description: 'We present ambatuCAM, a novel technique to tackle cheating in any exam environment.',
      presenter: 'Evan',
    },
    {
      title: 'Obfuscating Java to Compete With a Non-Compete',
      description: 'How to fight back against readable but legally unusable code by playing dirtier.',
      presenter: 'Aaryan',
    },
  ];
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

  {#each talks as talk, i (i)}
    <Talk
      {...talk}
    />
  {/each}
  <!-- <Wiki />
  <Cameron />
  <Evan />
  <Aaryan /> -->
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
