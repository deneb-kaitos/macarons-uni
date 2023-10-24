<script>
  export const prerender = true;

  import ContactUs from "../contact-us/ContactUs.svelte";
  import WeAreOpen from "../we-are-open/WeAreOpen.svelte";
  import Copyright from "../copyright/Copyright.svelte";
</script>
<style>
  footer {
    grid-area: app-footer;
    position: relative;
    display: grid;
    grid-template-rows: auto 6rem;
    grid-template-columns: 1fr 2fr 1fr; 
    grid-template-areas:
      'contact-us . we-are-open'
      'copyright copyright copyright'
    ;
    width: 75%;
    margin: 0 auto;

    & > div {
      display: flex;
      flex-direction: column;
    }

    & > #contact-us-container {
      grid-area: contact-us;
    }
    
    & > #we-are-open-container {
      grid-area: we-are-open;
    }

    & > #copyright-container {
      grid-area: copyright;
      justify-content: center;
      align-items: center;
    }
  }
</style>
<footer>
  <div id="contact-us-container">
    <ContactUs />
  </div>
  <div id="we-are-open-container">
    <WeAreOpen />
  </div>
  <div id="copyright-container">
    <Copyright />
  </div>
</footer>