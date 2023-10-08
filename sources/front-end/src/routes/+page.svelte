<script>
  import About from '$lib/pages/about/About.svelte';
  import Chef from '$lib/pages/chef/Chef.svelte';
  import Macarons from '$lib/pages/macarons/Macarons.svelte';
  import Torte from '$lib/pages/torte/Torte.svelte';
  import Legal from '$lib/pages/legal/Legal.svelte';

  export const prerender = true;
</script>

<style>
    article {
      background-color: brown;
      border-radius: 0.125rem;
      padding: min(0.5vh, 0.5vw);
      display: flex;
      flex-direction: column;
      flex: 1 0 auto;
      gap: 1vh;
    }
</style>
  <article>
    <About />
  </article>
  <article>
    <Chef />
  </article>
  <article>
    <Macarons />
  </article>
  <article>
    <Torte />
  </article>
  <article>
    <Legal />
  </article>