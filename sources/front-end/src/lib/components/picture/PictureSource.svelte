<script>
  /**
   * @type {string}
   */
  export let fileName;
  /**
   * @type {Number}
   */
  export let width;
  /**
   * @type {Number}
   */
  export let height;
</script>

<source
  srcset="https://fakeimg.pl/{width}x{height}?text={fileName}"
  {width}
  {height}
>