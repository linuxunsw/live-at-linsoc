<script>
  import { asset } from '$app/paths';
  import Background from './26t3w4/Background.svelte';
  import Hero from './26t3w4/Hero.svelte';
  import Talk from './26t3w4/Talk.svelte';
  import * as env from '$app/env';

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

  const siteName = 'Live@LNSC';
  const title = 'Live@LNSC // 26T3 Week 4';
  const description = 'Join us for 2 hours of student-run presentations, exploring the world of software engineering';
  const keywords = [
    'linux',
    'unsw',
    'linsoc',
    'live',
    'lightning talk',
    'event',
    'live at linsoc',
    'live at lnsc',
  ];
  // @ts-expect-error -- we give a fallback
  const pengwing = (env.DEPLOY_DOMAIN ?? '') + asset('/pengwing.png');
  // @ts-expect-error -- we give a fallback
  const socialsPreview = (env.DEPLOY_DOMAIN ?? '') + asset('/socials-preview.jpg');
</script>

<svelte:head>
  <title>{title}</title>
  <link rel="icon" type="image/png" href={pengwing}>
  <link rel="apple-touch-icon" type="image/png" href={pengwing}>
  <meta name="description" content={description} />
  <meta name="keywords" content={keywords.join(', ')}>
  <meta name="og:title" content={title} />
  <meta name="og:description" content={description} />
  <meta name="og:image" content={socialsPreview}>
  <meta name="og:locale" content="en_AU" />
  <meta name="og:site_name" content={siteName} />
  <!-- Let's be different syndrome -->
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:title" content={title}>
  <meta name="twitter:description" content={description} />
  <meta name="twitter:image" content={socialsPreview}>
</svelte:head>

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
