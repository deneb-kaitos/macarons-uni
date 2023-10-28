<script>
  import H1 from "$lib/controls/h1/H1.svelte";
  import H2 from "$lib/controls/h2/H2.svelte";
  import H3 from "$lib/controls/h3/H3.svelte";
  import ItemGrid from "../item-grid/ItemGrid.svelte";
  import Picture from "../picture/Picture.svelte";
  
  /**
   * @type {string}
   */
  export let href;
  /**
   * @type {string}
   */
  export let fileName; 
  /**
   * @type {string}
   */
  export let altText;
  /**
   * @type {string}
   */
  export let itemName;
  /**
   * @type {string}
   */
  export let subTitle;

  const components = [
    "component 0",
    "component 1",
    "component 2",
    "component 3",
  ];
  const allergens = [
    "allergen 0",
    "allergen 1",
    "allergen 2",
    "allergen 3",
  ];
</script>

<style>
  a {
    display: grid;
    grid-template-columns: 1fr 2fr;
    grid-auto-rows: 1fr;
    grid-template-areas:
      'item-picture item-info'
      'item-picture item-info'
      'item-picture contents'
      'item-picture allergens'
    ;
    column-gap: 1rem;
    padding: min(1vh, 1vw);
    background-color: white;
    color: var(--main-color);

    & > .item-picture {
      grid-area: item-picture;
      display: flex;
      justify-content: center;
      align-items: center;

      & > picture {
        aspect-ratio: 1 / 1;
        width: 100%;
        height: 100%;
        
        & > img {
          width: 100%;
          height: 100%;
        }
      }
    }

    & > .item-info {
      grid-area: item-info;
      display: flex;
      flex-direction: column;

      & > :is(h1, h2) {
        display: flex;
        justify-content: end;
        align-items: baseline;
        padding: 0;
      }

      & > :is(h1) {
        font-size: 12rem;
        line-height: 10rem;
      }

      & > :is(h2) {
        font-size: 2rem;
      }
    }
    
    & > .item-contents {
      grid-area: contents;
    }
    
    & > .item-allergens {
      grid-area: allergens;
    }
  }
</style>

<a {href}>
  <div class="item-picture">
    <Picture
      {fileName}
      {altText}
    />
  </div>
  <div class="item-info">
    <H1>{itemName}</H1>
    <H2>{subTitle}</H2>
  </div>
  <div class="item-contents">
    <ItemGrid
      title="components"
      items={components}
    />
  </div>
  <div class="item-allergens">
    <ItemGrid
      title="allergens"
      items={allergens}
    />
  </div>
</a>