<div class="grid mrjvs-grid-columns">
  <div class="column">
    <slot name="left" />
  </div>
  <div class="column offset">
    <slot name="right" />
  </div>
</div>

<style lang="scss">
  @use "sass:math";

  $spacing: 1.75rem;
  $offset: 6rem;

  $spacing_halved: math.div($spacing, 2);
  .grid {
    display: grid;
    grid-template-columns: 1fr 1fr;

    .column {
      padding-left: 0;
      padding-right: $spacing_halved;

      &.offset {
        padding-left: $spacing_halved;
        padding-right: 0;
        padding-top: $offset;
      }
    }
  }

  :global(.mrjvs-grid-columns > .column > *) {
    display: flex;
    flex-direction: column;
  }

  :global(.mrjvs-grid-columns > .column > * > *) {
    margin-bottom: $spacing;
  }
</style>
