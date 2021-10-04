<p>
  <slot />
</p>

<style lang="scss">
  @use 'colors' as c;

  p {
    color: c.$text_paragraph;
    text-align: left;
    line-height: 1.55;
    width: 100%;
    max-width: 34rem;
    margin-bottom: 1rem;
  }
</style>
