<script>
  import H1 from "$lib/controls/h1/H1.svelte";
</script>
<style>
  section {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: 1fr;
    grid-template-areas:
      'step0 step1 step2'
    ;
    gap: 1rem;
    min-height: 25vh;

    & > a {
      display: grid;
      grid-template-columns: auto 1fr 1fr;
      grid-template-rows: auto 0 1fr;
      grid-template-areas:
        'picture picture picture'
        'title title title'
        'description description description'
      ;
      padding: max(1vh, 1vw) max(1vh, 1vw);
      background-color: white;
      filter: opacity(0.98);

      & > img {
        grid-area: picture;
        width: 100%;
        height: 100%;
      }

      & > h1 {
        grid-area: title;
        display: flex;
        bottom: 7vh;
        height: 5vh;
        justify-content: center;
        align-items: center;

        background-color: white;
      }
      
      & > div {
        grid-area: description;
      }
    }

    & > .step0 {
      grid-area: step0;
    }

    & > .step1 {
      grid-area: step1;
    }
  
    & > .step2 {
      grid-area: step2;
    }
  }

  section:hover a:not(:hover) {
    filter: opacity(0.95) blur(1px);
  }
  section:hover a:hover {
    filter: opacity(1.0) blur(0);

    & > img {
      filter: drop-shadow(0 0 0.25rem var(--theme-darkest_white));
    }
  }
</style>

<section>
  <a href="/uni/complete-macarons" class="step0">
    <img src="https://fakeimg.pl/600x600" width="600px" height="600px" alt="step 0" />
    <H1>
     macarons 
    </H1>
    <div>some description</div>
  </a>
  <a href="/uni/macarons-caps" class="step1">
    <img src="https://fakeimg.pl/600x600" width="600px" height="600px" alt="step 1" />
    <H1>
      macaron caps
    </H1>
    <div>some description</div>
  </a>
  <a href="/uni/torten" class="step2">
    <img src="https://fakeimg.pl/600x600" width="600px" height="600px" alt="step 2" />
    <H1>
      cakes
    </H1>
    <div>some description</div>
  </a>
</section>