<script>
// @ts-nocheck

  import {
    onMount,
    onDestroy,
  } from 'svelte';
  import {
    browser as isInBrowser,
  } from '$app/environment';
  import PictureSource from './PictureSource.svelte';
  /**
   * @type {string}
   */
  export let fileName;
  /**
   * @type {Array<string>}
   */
  const fileExtensions = ['jpg', 'avif', 'webp'];
  /**
   * @type {Array<object>}
   */
  const fileDimensions = [
    {
      w: 1000,
      h: 1000,
    },
    {
      w: 900,
      h: 900,
    },
    {
      w: 800,
      h: 800,
    },
    {
      w: 700,
      h: 700,
    },
  ];
  /**
   * @type {string}
   */
  export let altText;

  /**
   * @type {Array<object>}
   */
  let pictureSources = [];
  /**
   * builds a single source element
   * @param file {string | null }
   * @param extensions {Array<string>}
   * @param dimensions {Array<object>}
   */
  const renderSources = (file = null, extensions = [], dimensions = []) => {
    if (file === null || extensions.length === 0 || dimensions.length === 0) {
      return;
    }

    for (const extension of extensions) {
      for (const dimension of dimensions) {
        pictureSources.push({
          extension,
          dimension,
        });
      }
    }

    console.debug(pictureSources);

    pictureSources = pictureSources;

  };

  onMount(() => {
    renderSources(fileName, fileExtensions, fileDimensions);
  });
</script>

<picture>
  {#each pictureSources as pictureSource}
    <source
      srcset="https://fakeimg.pl/{pictureSource.dimension.w}x{pictureSource.dimension.h}?text={fileName}.{pictureSource.extension}"
      width="{pictureSource.dimension.w}"
      height="{pictureSource.dimension.h}"
    >
  {/each}
  <img src="https://fakeimg.pl/100x100?text={fileName}" width="100px" height="100px" alt="{altText}" />
</picture>