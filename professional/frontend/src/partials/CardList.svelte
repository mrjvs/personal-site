<script>
  import ColumnGrid from "../components/layout/ColumnGrid.svelte";
  import Card from "../components/ui/Card.svelte";
  import AmBoats from "../components/ui/cardHeadings/AMBoats.svelte";
  import Designcourse from "../components/ui/cardHeadings/Designcourse.svelte";
  import Pretendo from "../components/ui/cardHeadings/Pretendo.svelte";
  import Heading from "../components/ui/Heading.svelte";
  import Link from "../components/ui/Link.svelte";
  import MoreCard from "../components/ui/MoreCard.svelte";
  import Paragraph from "../components/ui/Paragraph.svelte";
</script>

<ColumnGrid>
  <div slot="left">
    <Card>
      <div slot="head">
        <Designcourse />
      </div>

      <Heading size="h2">Designcourse</Heading>
      <Paragraph>
        Gary has over 20 years experience as a UI/UX Designer & Frontend
        Developer. After enjoying a freelance career that lasted over a decade,
        Gary’s content has reached millions of people and helped countless
        individuals establish careers.
      </Paragraph>
      <Link type="internal" to="#" color="green" arrow>How I did it</Link>
    </Card>
    <Card>
      <div slot="head">
        <AmBoats />
      </div>

      <Heading size="h2">AM boats</Heading>
      <Paragraph>
        Gary has over 20 years experience as a UI/UX Designer & Frontend
        Developer. After enjoying a freelance career that lasted over a decade,
        Gary’s content has reached millions of people and helped countless
        individuals establish careers.
      </Paragraph>
      <Link type="internal" to="#" color="gray" arrow>How we did it</Link>
    </Card>
  </div>
  <div slot="right">
    <Card>
      <div slot="head">
        <Pretendo />
      </div>

      <Heading size="h2">Pretendo</Heading>
      <Paragraph>
        Gary has over 20 years experience as a UI/UX Designer & Frontend
        Developer. After enjoying a freelance career that lasted over a decade,
        Gary’s content has reached millions of people and helped countless
        individuals establish careers.
      </Paragraph>
      <Link type="internal" to="#" color="pink" arrow>How I did it</Link>
    </Card>
    <MoreCard />
  </div>
</ColumnGrid>
