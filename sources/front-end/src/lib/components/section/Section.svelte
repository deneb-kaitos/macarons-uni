<script>
  export let title;
</script>

<style>
  a {
    display: flex;
    flex: 1 0 auto;
    padding: 0 10vw;

    & h1 {
      display: flex;
      flex-direction: row;
      flex: 1 0 auto;
      justify-content: flex-end;
      font-variant: all-petite-caps;
      align-items: center;

      width: 100%;
      height: 100%;

    }

   & picture {
      position: absolute;
      top: 0;
      bottom: 0;
      left: 0;
      right: 0;
      width: 100%;
      height: 100%;
    }
  }

  a:visited {
    color: var(--theme-black);
  }

</style>

<a href="/macaroons/{title}">
  <picture>
    <source srcset="https://fakeimg.pl/371x100" media="(orientation: portrait)" />
    <img src="https://fakeimg.pl/371x100" width="371px" height="100px" alt="the Chef" />
  </picture>
  <h1>{title}</h1>
</a>