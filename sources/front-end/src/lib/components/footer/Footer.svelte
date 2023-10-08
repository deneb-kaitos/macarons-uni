<script>
  import MenuIcon from "$lib/icons/MenuIcon.svelte";
</script>
<style>
  footer {
    position: sticky;
    bottom: 0px;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    padding: min(0.5vh, 0.5vw);
    background-color: aquamarine;
    height: var(--footer-height);

    & button {
      display: flex;
      justify-content: center;
      align-items: center;
      border-radius: 50%;
    }
  }
</style>
<footer>
  <button>
    <MenuIcon />
  </button>
</footer>