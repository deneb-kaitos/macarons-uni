<style>
  h2 {
    padding: 1rem 0;
    font-variant: all-petite-caps;
    font-size: 2rem;
  }

  @supports (font-variation-settings: normal) {
    h1 {
      font-variation-settings:
        "wght" 700
      ;
      font-feature-settings:
        "case" 0,
        "cpsp" 1,
        "dlig" 0,
        "frac" 0,
        "dnom" 0,
        "numr" 0,
        "salt" 1,
        "subs" 0,
        "sups" 0,
        "tnum" 1,
        "zero" 1,
        "ss01" 1,
        "ss02" 1,
        "ss03" 1,
        "ss04" 0,
        "cv01" 0,
        "cv02" 0,
        "cv03" 0,
        "cv04" 0,
        "cv05" 0,
        "cv06" 0,
        "cv07" 1,
        "cv08" 0,
        "cv09" 0,
        "cv10" 0,
        "cv11" 0,
        "calt" 0,
        "ccmp" 0,
        "kern" 0;
    }
  }
</style>

<h2>
  <slot />
</h2>