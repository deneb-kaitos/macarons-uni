<script>
  export const prerender = true;
</script>

<style>
  article {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr;
    grid-template-areas:
    'photo text';
    gap: min(0.5vh, 0.5vw);

    & picture {
      grid-area: photo;
      aspect-ratio: 2/3 auto;
    }

    & section {
      grid-area: text;
    }
  }
</style>

<article>
  <picture>
    <source srcset="https://fakeimg.pl/180x210" media="(orientation: portrait)" />
    <img src="https://fakeimg.pl/180x210" width="180px" height="210px" alt="the Chef" />
  </picture>
  <section>bla-bla-bla bla-bla-bla...</section>
</article>