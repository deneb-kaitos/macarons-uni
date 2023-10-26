<script>
  import H1 from "$lib/controls/h1/H1.svelte";

</script>

<style>
  section {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: auto 1fr;
    grid-template-areas:
      'header header header'
      'fav0 fav1 fav2'
    ;
    gap: 1rem;

    & > h1 {
      grid-area: header;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    & > div {
      display: flex;
      flex-direction: column;
      align-items: center;
    
      & > h2 {
        position: absolute;
        bottom: 3vh;
        width: 100%;
        height: 5vh;
        display: flex;
        justify-content: center;
        align-items: center;

        background-color: white;
      }

      & > img {
        width: 100%;
        height: 100%;
      }
    }

    & > .fav0 {
      grid-area: fav0;
    }
     
    & > .fav1 {
      grid-area: fav1;
    }

    & > .fav2 {
      grid-area: fav2;
    }
  }
</style>

<section>
  <H1>all time favorites</H1>
  <div class="fav0">
    <img src="https://fakeimg.pl/800x800" width="800px" height="800px" alt="0" />
    <h2>some macaron</h2>
  </div>
  <div class="fav1">
    <img src="https://fakeimg.pl/800x800" width="800px" height="800px" alt="1" />
    <h2>some cap</h2>
  </div>
  <div class="fav2">
    <img src="https://fakeimg.pl/800x800" width="800px" height="800px" alt="2" />
    <h2>some cake</h2>
  </div>
</section>