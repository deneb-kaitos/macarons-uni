<script>
  import AboutSection from '$lib/mainPageSections/aboutSection/AboutSection.svelte';
  import ChefSection from '$lib/mainPageSections/chefSection/ChefSection.svelte';
  import MacaronsSection from '$lib/mainPageSections/macaronsSection/MacaronsSection.svelte';
  import LegalSection from '$lib/mainPageSections/legalSection/LegalSection.svelte';
	import TorteSection from '$lib/mainPageSections/torteSection/TorteSection.svelte';
  import MainBanner from '$lib/components/main-banner/MainBanner.svelte';
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
      width: 75%;
      margin: 0 auto;
    }
    
    .banner {
      width: 100%;
      height: 50vh;
      background-color: yellowgreen; 
    }
</style>
  <article class="banner">
    <MainBanner />
  </article>
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