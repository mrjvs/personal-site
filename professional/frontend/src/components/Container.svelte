<div>
  <slot />
</div>

<style lang="scss">
  @use 'sizes' as size;

  div {
    width: 100%;
    max-width: size.$breakpoint_md;
    padding: 1rem 2rem;
    margin: 0 auto;
  }
</style>
