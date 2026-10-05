<script lang="ts">
  type Props = {
    title: string,
    description: string,
    presenter: string,
  };
  const { title, description, presenter }: Props = $props();

  const rotation = (Math.random() - 0.5) * 2;
  const multiplier = Math.random() - 2;
</script>

<div class="talk">
  <h3 style:--rot={rotation}>{title}</h3>
  <p style:--rot={rotation * multiplier}>{description}</p>
  <p style:--rot={rotation * multiplier ** 2}>Presented by {presenter}</p>
</div>
<style>
  .talk {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  h3, p {
    transition: all 0.1s;
    transform: rotate(calc(var(--rot) * 1deg));
  }
  .talk:hover h3, .talk:hover p {
    transform: rotate(calc(var(--rot) * 0.5deg));
  }
  h3 {
    margin: 0;
    margin-top: 50px;
  }
  p {
    margin: 5px;
    max-width: min(100%, 60ch);
  }
</style>
