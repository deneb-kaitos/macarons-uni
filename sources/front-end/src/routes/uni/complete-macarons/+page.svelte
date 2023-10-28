<script>
  import ItemInfo from "$lib/components/item-info/ItemInfo.svelte";
</script>
<style>
  article {
    display: grid;
    grid-template-columns: 1fr;
    grid-auto-rows: 1fr;
    margin: 0 10%;
    row-gap: 1rem;
  } 
</style>

<article>
  <ItemInfo
    href="/uni/complete-macarons/macaron_0"
    fileName="macaron_0"
    altText="macaron 0"
    itemName="macaron 0"
    subTitle="This is the strong Three Wood Whisky from Auchentoshan. After about 10 years of maturation in ex-bourbon casks, the whisky is matured for 2 years in an oloroso sherry cask before being matured for a further 6 months in a sweet Pedro Ximénez sherry cask."
  />
  <ItemInfo
    href="/uni/complete-macarons/macaron_1"
    fileName="macaron_1"
    altText="macaron 1"
    itemName="macaron 1"
    subTitle="This is the strong Three Wood Whisky from Auchentoshan. After about 10 years of maturation in ex-bourbon casks, the whisky is matured for 2 years in an oloroso sherry cask before being matured for a further 6 months in a sweet Pedro Ximénez sherry cask."
  />
  <ItemInfo
    href="/uni/complete-macarons/macaron_2"
    fileName="macaron_2"
    altText="macaron 2"
    itemName="macaron 2"
    subTitle="This is the strong Three Wood Whisky from Auchentoshan. After about 10 years of maturation in ex-bourbon casks, the whisky is matured for 2 years in an oloroso sherry cask before being matured for a further 6 months in a sweet Pedro Ximénez sherry cask."
  />
</article>