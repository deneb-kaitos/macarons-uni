<script>
  import H3 from "$lib/controls/h3/H3.svelte";
  /**
   * @type {string}
   */
  export let title;
  /**
   * @type {Array<string>}
   */
  export let items;
</script>

<style>
  div:not(.grid-item) {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: 1fr;
    grid-template-areas:
      'title title'
    ;
    gap: 1rem;
  
    & > :is(h3) {
      grid-area: title;
    }
  }
</style>

<div>
  <H3>{title}</H3>
  {#each items as item}
    <div class="grid-item">{item}</div>  
  {/each}
</div>