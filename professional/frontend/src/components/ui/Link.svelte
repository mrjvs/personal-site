<script>
  import { Link } from "svelte-routing";
  import Icon from "svelte-icon";
  import arrowIcon from "../../../assets/icons/arrow.svg";

  // supported: external, internal
  export let type = "external";

  // supported: newtab, replace
  export let target = "newtab";

  // the link
  export let to;

  // have an arrow?
  export let arrow = false;

  // color of the link: green, pink, gray
  export let color = "green";

  const targetMap = {
    newtab: "_blank",
    replace: "_self",
  };
  let realTarget = targetMap[target];
  $: realTarget = targetMap[target];

  let classList = "";
  $: classList = "link mrjvs-link color-" + color;
</script>

{#if type === "external"}
  <a href={to} target={realTarget} class={classList}
    ><slot />{#if arrow}<Icon
        class="arrow"
        fill="none"
        stroke-width="3"
        data={arrowIcon}
      />{/if}</a
  >
{:else if type === "internal"}
  <Link {to} class={classList}
    ><slot />{#if arrow}<Icon
        class="arrow"
        fill="none"
        stroke-width="3"
        data={arrowIcon}
      />{/if}</Link
  >
{:else}
  <span class={classList}
    ><slot />{#if arrow}<Icon
        class="arrow"
        fill="none"
        stroke-width="3"
        data={arrowIcon}
      />{/if}</span
  >
{/if}

<style lang="scss">
  @use 'colors' as c;
  $colors: ".color-green" c.$text_green c.$text_green_light,
    ".color-pink" c.$text_pink c.$text_pink_light,
    ".color-gray" c.$text_gray c.$text_gray_light;

  @each $name, $color, $color_hover in $colors {
    :global(.mrjvs-link#{$name}),
    .link#{$name} {
      &,
      &:visited,
      &:focus {
        color: $color;
      }

      &:hover {
        color: $color_hover;
      }
    }
  }

  :global(.mrjvs-link),
  .link {
    display: inline-flex;
    align-items: flex-end;

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

  :global(.mrjvs-link > .arrow),
  .link > :global(.arrow) {
    margin-bottom: 0.1em;
    display: inline-block;
    margin-left: 0.3em;
    transition: transform 100ms ease-in-out;
  }
  :global(.mrjvs-link:hover > .arrow),
  .link:hover > :global(.arrow) {
    transform: translateX(0.2rem);
  }
</style>
