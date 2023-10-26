<script>
  import H1 from "$lib/controls/h1/H1.svelte";
  import H2 from "$lib/controls/h2/H2.svelte";
</script>
<style>
  section {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: 1fr;
    grid-template-areas:
      'picture text'
    ;

    background-color: bisque;

    & > img {
      grid-area: picture;
    }

    & > .text {
      grid-area: text;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: end;
      padding: 0 3vw;
    }
  }
</style>

<section>
  <img src="https://fakeimg.pl/1500x400" width="1500px" height="400px" alt="we deliver" />
  <div class="text">
    <H1>
      we deliver
    </H1>
    <H2>if you are in Berlin</H2>
  </div>
</section>