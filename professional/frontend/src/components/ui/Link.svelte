<script>
  import { Link } from "svelte-routing";

  // supported: external, internal
  export let type = "external";

  // supported: newtab, replace
  export let target = "newtab";

  // the link
  export let to;

  const targetMap = {
    newtab: "_blank",
    replace: "_self",
  };
  let realTarget = targetMap[target];
  $: realTarget = targetMap[target];
</script>

{#if type === "external"}
  <a href={to} target={realTarget} class="link"><slot /></a>
{:else if type === "internal"}
  <Link {to} class="mrjvs-link"><slot /></Link>
{:else}
  <span class="link"><slot /></span>
{/if}

<style lang="scss">
  @use 'colors' as c;

  :global(.mrjvs-link),
  .link {
    &,
    &:visited,
    &:focus {
      color: c.$text_green;
      font-weight: bold;
      text-decoration: none;
    }

    &:hover {
      color: c.$text_green_light;
      text-decoration: underline;
    }
  }
</style>
