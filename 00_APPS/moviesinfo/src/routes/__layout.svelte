<script>
  import "../styles/global.css";
  import Nav from "../components/Nav.svelte";
</script>

<svelte:head>
  <title>Movie Info</title>
  <link rel="shortcut icon" href="favicon.ico" type="image/x-icon" />
</svelte:head>
<div class="app">
  <Nav />
  <slot />
</div>
