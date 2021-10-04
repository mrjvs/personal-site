<nav>
  <div class="left">
    <slot />
  </div>
  <div class="right">
    <slot name="right" />
  </div>
</nav>

<style lang="scss">
  @use 'sizes' as sizes;

  nav {
    margin-left: #{-1 * sizes.$nav_link_x};
    margin-right: #{-1 * sizes.$nav_link_x};

    &,
    .left,
    .right {
      display: flex;
    }

    .left {
      flex: 1;
    }
  }
</style>
