<script>
  import Heading from "./Heading.svelte";
  import Paragraph from "./Paragraph.svelte";
  import Icon from "svelte-icon";
  import plusIcon from "../../../assets/icons/plus.svg";
</script>

<section class="card">
  <div class="icon">
    <Icon
      class="plus"
      fill="currentColor"
      viewBox="0 0 23.769 23.769"
      style="height: 1em; width: 1em"
      data={plusIcon}
    />
  </div>
  <div class="text">
    <span class="title"><Heading size="2">More to come</Heading></span>
    <Paragraph
      >I'm working on some exciting projects that I having a blast working on</Paragraph
    >
  </div>
</section>

<style lang="scss">
  @use 'colors' as c;

  .card {
    background-image: url("data:image/svg+xml,%3csvg width='100%25' height='100%25' xmlns='http://www.w3.org/2000/svg'%3e%3crect width='100%25' height='100%25' fill='none' rx='15' ry='15' stroke='%233B3E46' stroke-width='5' stroke-dasharray='15%2c 14' stroke-dashoffset='20' stroke-linecap='square'/%3e%3c/svg%3e");
    border-radius: 15px;
    color: c.$text_card_body;
    overflow: hidden;
    opacity: 0.47;
    padding: 7rem 3rem;
    transition: opacity 100ms ease-in-out;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    &:hover {
      opacity: 1;
    }
  }

  .text {
    text-align: center;
    width: 100%;
    max-width: 18rem;
    margin: auto;
    color: #b3b9d1;

    .title {
      color: #fff;
    }
  }

  .icon {
    background-color: #282a33;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 4rem;
    width: 4rem;
    margin-bottom: 2rem;
    color: #99ffa6;

    font-size: 1.4rem;
  }
</style>
