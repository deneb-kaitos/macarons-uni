<script>
  export const prerender = true;
  import MenuIcon from "$lib/icons/MenuIcon.svelte";
</script>
<style>
  footer {
    grid-area: app-footer;
    position: sticky;
    bottom: 0px;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    padding: min(0.5vh, 0.5vw);
    /* background-color: aquamarine; */
    height: var(--footer-height);
    flex: 1 0 auto;

    & button {
      display: flex;
      justify-content: center;
      align-items: center;
      border-radius: 50%;
    }
  }
</style>
<footer>
  <!-- <button>
    <MenuIcon />
  </button> -->
</footer>