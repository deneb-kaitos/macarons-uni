<script>
  import Header from '$lib/components/header/Header.svelte';
  import Footer from '$lib/components/footer/Footer.svelte';
</script>
<Header />
<main>
  <slot />
</main>
<Footer />