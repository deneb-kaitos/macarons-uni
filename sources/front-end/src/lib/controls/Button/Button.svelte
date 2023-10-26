<script>
// @ts-nocheck

  /**
	 * @type {string}
	 */
   export let buttonType;
  /**
   * @type {('button'|'submit'|'reset'|null|undefined)}
   */
  export let buttonText;
</script>

<style>
  button {
    background-color: var(--theme-glacier);
    border: none;
    border-radius: max(0.125vh, 0.125vw);
    padding: max(0.5vh, 0.5vw);
    max-height: 6rem;
    color: var(--theme-white);
  }
</style>

<button type="{buttonType}">{buttonText}</button>