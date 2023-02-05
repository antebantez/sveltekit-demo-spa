<script>
// @ts-nocheck

  import {
    Collapse,
    Navbar,
    NavbarToggler,
    NavbarBrand,
    Nav,
    NavItem,
    NavLink
  } from 'sveltestrap';

  let isOpen = false;

  function handleUpdate(event) {
    isOpen = event.detail.isOpen;
  }
</script>

<Navbar color="light" light expand="md">
  <NavbarBrand id="anton" href="/">NewsFeed</NavbarBrand>
  <NavbarToggler on:click={() => (isOpen = !isOpen)} />
  <Collapse {isOpen} navbar expand="md" on:update={handleUpdate}>
    <Nav class="me-auto" navbar>
      <NavItem>
        <NavLink href="/">Home</NavLink>
      </NavItem>
      <NavItem>
        <NavLink href="/posts/">Posts</NavLink>
      </NavItem>
      <NavItem>
        <NavLink href="/about/">About</NavLink>
      </NavItem>
    </Nav>
  </Collapse>
</Navbar>

<style>
  :global(.nav){
    background: gray;
  }

  :global(.nav){
    color: rgb(36, 36, 36);
  }
</style>