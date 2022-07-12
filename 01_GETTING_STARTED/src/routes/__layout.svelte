<script>
  import "../styles/global.css";
  import Footer from "../components/Footer.svelte";
  import Nav from "../components/Nav.svelte";
</script>

<svelte:head>
  <title>My app</title>
  <link rel="shortcut icon" href="favicon.ico" type="image/x-icon" />
</svelte:head>
<Nav />
<slot />
<Footer />
