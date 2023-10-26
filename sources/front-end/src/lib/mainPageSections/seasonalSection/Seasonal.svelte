<script>
  export const prerender = true;
  import H1 from "$lib/controls/h1/H1.svelte";
</script>

<style>
  section {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: 1fr;
    grid-template-areas:
      'card picture'
    ;
    column-gap: 2vw;
  
    & > .card { 
      grid-area: card;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      background-color: white;
    }

    & > .picture {
      grid-area: picture;
      display: flex;
      justify-content: center;
      align-items: center;
      width: 100%;

      & > img {
        display: flex;
        flex: 1 0 auto;
      }
    }
  }
</style>

<section>
  <div class="card">
    <H1>
      special of the week
    </H1>
    <h2>
      your new guilty pleasure
    </h2>
  </div>
  <div class="picture">
    <img src="https://fakeimg.pl/1400x400" width="1400px" height="400px" alt="seasonal" />
  </div>
</section>