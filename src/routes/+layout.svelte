<script>
  // const props = $props();
  // console.log({props});
  const { children } = $props();
</script>

<nav>
  <a href="/">
    <h1>Hello World!</h1>
  </a>
  <a href="/about">About</a>
  <a href="/stuff">Stuff</a>
  <a href="/plot">Plot</a>
  <a href="/random">Random</a>
</nav>
{@render children()}

<style>
  nav {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 1rem;
    padding: 1rem;
    background: #fefefe;
    border-width: 2px;
    border: solid salmon;
  }
</style>
