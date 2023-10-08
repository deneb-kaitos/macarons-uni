<script>
  import AboutSection from '$lib/mainPageSections/aboutSection/AboutSection.svelte';
  import ChefSection from '$lib/mainPageSections/chefSection/ChefSection.svelte';
  import MacaronsSection from '$lib/mainPageSections/macaronsSection/MacaronsSection.svelte';
  import LegalSection from '$lib/mainPageSections/legalSection/LegalSection.svelte';
	import TorteSection from '$lib/mainPageSections/torteSection/TorteSection.svelte';

  export const prerender = true;
</script>

<style>
    article {
      /* background-color: brown; */
      border-radius: 0.125rem;
      padding: min(0.5vh, 0.5vw);
      display: flex;
      flex-direction: column;
      flex: 1 0 auto;
      gap: 1vh;
    }
</style>
  <article>
    <AboutSection />
  </article>
  <article>
    <ChefSection />
  </article>
  <article>
    <MacaronsSection />
  </article>
  <article>
    <TorteSection />
  </article>
  <article>
    <LegalSection />
  </article>