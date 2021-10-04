<script>
  import NavBar from "components/nav/NavBar.svelte";
  import NavbarLink from "components/nav/NavbarLink.svelte";
</script>

<NavBar>
  <NavbarLink important>Jelle van Snik</NavbarLink>
  <NavbarLink>Link 1</NavbarLink>
  <NavbarLink>Link 2</NavbarLink>

  <div slot="right">
    <NavbarLink>Right link</NavbarLink>
  </div>
</NavBar>
