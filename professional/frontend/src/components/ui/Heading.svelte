<script>
  export let size = "h1";
  export let subhead = "";
</script>

<div>
  <h1 class={size}><slot /></h1>
  {#if subhead.length > 0}
    <h4>{subhead}</h4>
  {/if}
</div>

<style lang="scss">
  @use 'colors' as c;
  @use 'sizes' as sizes;

  h1 {
    font-size: sizes.$text_hero;
    color: c.$text_white;
    font-weight: bold;
    margin: 0;

    &.h2 {
      font-size: sizes.$text_card;
    }
  }

  h4 {
    font-size: sizes.$text_subheading;
    color: c.$text_green;
    margin: 0.3rem 0 0 0;
  }

  div {
    margin-bottom: 1.2rem;
  }
</style>
