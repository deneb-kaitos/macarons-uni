<script>
  export const prerender = true;
</script>

<style>
  div {
    display: grid;
    grid-template-columns: 1fr 2fr;
    grid-template-rows: 1fr;
    grid-template-areas:
    'photo text';
    gap: min(0.5vh, 0.5vw);
    padding: 1rem;

    background-color: white;

    & picture {
      grid-area: photo;
      aspect-ratio: 2/3 auto;
      display: flex;
      justify-content: center;
      align-items: start;

      & > img {
        width: 100%;
        height: 100%;
      }
    }

    & section {
      grid-area: text;
    }
  }
</style>

<div>
  <picture>
    <source srcset="https://fakeimg.pl/600x800" media="(orientation: portrait)" />
    <img src="https://fakeimg.pl/600x800" width="600px" height="800px" alt="the Chef" />
  </picture>
  <section>
    about Alsuh ( CV )
  <section>
</div>