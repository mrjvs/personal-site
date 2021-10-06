<script>
  import Navbar from "partials/Navbar.svelte";
  import Container from "../components/Container.svelte";
  import CardList from "../partials/CardList.svelte";
  import Hero from "../partials/Hero.svelte";

  // needed for SSR
  export let location = "";
</script>

<svelte:head>
  <title>Home | mrjvs</title>
</svelte:head>

<Container>
  <Navbar />
  <Hero />
  <CardList />
</Container>
