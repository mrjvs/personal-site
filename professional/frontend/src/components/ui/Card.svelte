<section class="card">
  <div>
    <slot name="head" />
  </div>
  <div class="body">
    <slot />
  </div>
</section>

<style lang="scss">
  @use 'colors' as c;

  .card {
    background-color: c.$bg_gray_300;
    border-radius: 15px;
    color: c.$text_card_body;

    .body {
      padding: 3rem;
    }
  }
</style>
