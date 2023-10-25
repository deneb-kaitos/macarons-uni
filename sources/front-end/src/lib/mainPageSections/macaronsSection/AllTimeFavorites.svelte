<script>
  export const prerender = true;

  import Section from "$lib/components/section/Section.svelte";
</script>

<style>
    section {
      height: 100px;
      background-color: beige; 
      display: flex;
      flex-direction: column;
      justify-content: center;
    }
</style>

  <section>
    <Section
      title="caps"
    />
  </section>
  <section>
    <Section
      title="fillings"
    />
  </section>