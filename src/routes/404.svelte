<script lang="ts">
    import Bg from '../lib/Bg.svelte';
</script>

<svelte:head>
    <title>Page not found | GunnHacks 8.0</title>
    <meta name="description" content="Make, Build, Create & Learn. It’s GunnHacks 8.0, Gunn’s 24‑hour high school hackathon.">
</svelte:head>

<Bg />
<main>
    <img src="lambda-sad.png" alt="lambda frown">
    <h2>We couldn't find the page you requested!</h2>
    <p>Check your url and try again?</p>
    <a href="/">Go home</a>
</main>

<style lang="scss">
  main {
    height: 100vh;
    color: black;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    img {
      height: 5rem;
    }
    h2 {
      margin: 0.75rem 0;
    }
    p {
      margin: 0.25rem 0;
    }
  }
</style>
