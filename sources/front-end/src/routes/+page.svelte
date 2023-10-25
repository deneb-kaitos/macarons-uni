<script>
  import AboutSection from '$lib/mainPageSections/aboutSection/AboutSection.svelte';
  import ChefSection from '$lib/mainPageSections/chefSection/ChefSection.svelte';
  import AllTimeFavorites from '$lib/mainPageSections/macaronsSection/AllTimeFavorites.svelte';
	import SeasonalSection from '$lib/mainPageSections/seasonalSection/Seasonal.svelte';
  import MainBanner from '$lib/components/main-banner/MainBanner.svelte';
  import WeDeliver from '$lib/mainPageSections/weDeliver/WeDeliver.svelte';
</script>

<style>
    article {
      /* background-color: brown; */
      border-radius: 0.125rem;
      /* padding: min(0.5vh, 0.5vw); */
      display: flex;
      flex-direction: column;
      flex: 1 0 auto;
      margin: 0 10%;
    }
    
    .banner {
      width: 100%;
      height: 50vh;
      background-color: yellowgreen; 
      margin: 0;
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
    <AllTimeFavorites />
  </article>
  <article>
    <SeasonalSection />
  </article>
  <article>
    <WeDeliver />
  </article>