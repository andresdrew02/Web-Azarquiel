<script>
  import Footer from "../components/Footer.svelte";
  import Navbar from "../components/Navbar.svelte";
</script>

<main>
  <Navbar />
  <div class="slot">
    <slot />
  </div>
  <Footer />
</main>

<style>
  :global(body) {
    font-family: "Raleway", sans-serif;
    margin: 0;
    padding: 0;
  }

  main {
    display: flex;
    flex-direction: column;
    height: 100vh;
  }

  .slot {
    flex-grow: 1;
  }
</style>
