<script>
  import Heading from "../components/ui/Heading.svelte";
  import Paragraph from "../components/ui/Paragraph.svelte";
  import Link from "../components/ui/Link.svelte";
  import HoverableImage from "../components/image/HoverableImage.svelte";
  import LeftRight from "../components/layout/LeftRight.svelte";
</script>

<div class="wrapper">
  <LeftRight>
    <div slot="left">
      <Heading subhead="Web dev & designer">I am Jelle van Snik</Heading>
      <Paragraph>
        Currently working on
        <Link to="https://designcourse.com">
          designcourse, a UI/UX course platform
        </Link>
      </Paragraph>
      <Paragraph>
        After stumbling around with basic HTML/CSS in middle school, I decided
        to make it my job and been studying for it ever since. After stumbling
        around with basic HTML/CSS in middle school, I decided to make it my job
        and been studying for it ever since.
      </Paragraph>
      <Link type="external" target="replace" to="#id" arrow>Contact me</Link>
    </div>
    <div slot="right">
      <HoverableImage
        src="/images/my-only-good-picture.png"
        alt="Jelle van snik staring into the camera"
      />
    </div>
  </LeftRight>
</div>

<style lang="scss">
  .wrapper {
    margin: 4rem 0;
  }
</style>
