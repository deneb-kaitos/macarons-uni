<script>
  export const prerender = true;
</script>

<style>
  article {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 1fr;
    gap: min(0.5vh, 0.5vw);

    & section {
      height: 100px;
      background-color: beige; 
    }
  }
</style>

<article>
  <section>
    section #0
  </section>
  <section>
    section #1
  </section>
  <section>
    section #2
  </section>
  <section>
    section #3
  </section>
  <section>
    section #4
  </section>
  <section>
    section #5
  </section>
</article>