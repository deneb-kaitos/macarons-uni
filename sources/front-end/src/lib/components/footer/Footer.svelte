<script>
  export const prerender = true;

  import ContactUs from "../contact-us/ContactUs.svelte";
  import WeAreOpen from "../we-are-open/WeAreOpen.svelte";
</script>
<style>
  footer {
    grid-area: app-footer;
    position: relative;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr;
    width: 75%;
    margin: 0 auto;

    & > div {
      display: flex;
      /* background-color: brown; */
      flex-direction: column;
      padding-bottom: 1rem;
    }
  }
</style>
<footer>
  <div>
    <ContactUs />
  </div>
  <div>
    <WeAreOpen />
  </div>
</footer>