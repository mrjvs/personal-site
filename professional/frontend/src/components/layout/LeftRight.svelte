<div class="wrapper">
  <div class="left">
    <slot name="left" />
  </div>
  <div class="right">
    <slot name="right" />
  </div>
</div>

<style lang="scss">
  .wrapper {
    display: flex;
    flex-direction: row;
    align-items: center;

    .left,
    .right {
      display: flex;
      flex-direction: column;
      align-items: start;
    }

    .left {
      flex: 1;
    }
  }
</style>
