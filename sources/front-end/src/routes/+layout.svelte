<script>
  import Header from "$lib/components/header/Header.svelte";
  import Footer from "$lib/components/footer/Footer.svelte";
</script>
<style>
</style>
<Header />
<main>
  <slot />
</main>
<Footer />