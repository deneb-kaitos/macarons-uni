<script>
  import MainNavSection from "$lib/components/mainNavSection/MainNavSection.svelte";
</script>

<style>
  div {
    display: grid;
    grid-template-columns: 1fr;
    grid-auto-rows: 1fr;
    height: 100%;
    gap: 1vh;
    padding: min(0.5vw, 0.5vh);
    align-items: flex-start;
    justify-content: center;
  }
</style>
<div>
  <MainNavSection />
  <MainNavSection />
</div>