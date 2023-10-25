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

    & > div {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      grid-template-rows: auto 1fr 1fr;
      grid-template-areas:
        '. picture .'
        '. title .'
        'description description description'
      ;
      padding: max(1vh, 1vw) max(1vh, 1vw);
      background-color: white;

      & > img {
        grid-area: picture;
        width: 100%;
        height: 100%;
      }

      & > h1 {
        grid-area: title;
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
</style>

<section>
  <div class="step0">
    <img src="https://fakeimg.pl/200x200" width="200px" height="200px" alt="step 0" />
    <h1>
      title
    </h1>
    <div>some description</div>
  </div>
  <div class="step1">
    <img src="https://fakeimg.pl/200x200" width="200px" height="200px" alt="step 0" />
    <h1>
      title
    </h1>
    <div>some description</div>
  </div>
  <div class="step2">
    <img src="https://fakeimg.pl/200x200" width="200px" height="200px" alt="step 0" />
    <h1>
      title
    </h1>
    <div>some description</div>
  </div>
</section>