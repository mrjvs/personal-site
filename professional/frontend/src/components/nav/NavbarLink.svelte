<script>
  import { Link } from "svelte-routing";

  export let important = false;
  export let href = "";
  export let to = "";
</script>

<span class="item-container" class:important>
  {#if to.length == 0}
    <a class="item" {href}>
      <slot>My awesome link</slot>
    </a>
  {:else}
    <Link class="item" href={to}>
      <slot>My awesome link</slot>
    </Link>
  {/if}
</span>

<style lang="scss">
  @use 'colors' as c;

  .item-container {
    display: block;

    .item {
      padding: 0.8rem 1.4rem;
      display: inline-block;
      color: c.$text_body;
      cursor: pointer;
      transform: scale(1);
      transform-origin: center;
      transition: transform 50ms ease-in-out;
      text-decoration: none;

      &:hover {
        transform: scale(1.05);
        color: c.$text_white;
      }
    }

    &.important .item {
      font-weight: bold;
      color: c.$text_white;
    }
  }
</style>
