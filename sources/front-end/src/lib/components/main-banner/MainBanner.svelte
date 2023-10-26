<script>
  import H1 from "$lib/controls/h1/H1.svelte";
  import H2 from "$lib/controls/h2/H2.svelte";
</script>
<style>
  div {
    top: 25%;

    & > h2 {
      font-size: 4rem;
    }
  
    & > h1 {
      font-size: 6rem;
    }
  }
</style>

<div>
  <H2>
    open for delivery & pick up
  </H2>
  <H1>
    get it while it's hot
  </H1>
</div>