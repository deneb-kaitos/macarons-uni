<script>
  /**
   * @type string
   */
  export let forElement;
  /**
   * @type string
   */
  export let text;
</script>

<style>
  label {
    font-size: 1rem;
    color: var(--theme-light_gray_bright);
    font-variant: all-petite-caps;
  }
</style>

<label for="{forElement}">{text}</label>