<script>
  import { Router, Link, Route } from "svelte-routing";
  import Home from "routes/Home.svelte";
  import NotFound from "routes/404.svelte";
  import Designcourse from "routes/posts/Designcourse.svelte";

  export let url = "";
</script>

<Router {url}>
  <div class="container">
    <Route path="/" component={Home} />
    <Route path="/work/designcourse" component={Designcourse} />
    <Route path="*" component={NotFound} />
  </div>
</Router>

<style lang="scss">
  @use 'colors' as c;

  .container {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    width: 100%;
    min-height: 100%;
    overflow-x: hidden;
    color: c.$text_paragraph;
  }
</style>
