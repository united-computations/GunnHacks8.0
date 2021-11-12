<script lang="ts" context="module">
    export function load(res) {
        return { props: res }
    }
</script>

<script lang="ts">
    import Bg from '../lib/Bg.svelte';

    export let error: Error;
    export let status: number;
</script>

<svelte:head>
    {#if status === 404}
        <title>Page not found | GunnHacks 8.0</title>
    {:else}
        <title>{status} | GunnHacks 8.0</title>
    {/if}
    <meta name="description" content="Make, Build, Create & Learn. It’s GunnHacks 8.0, Gunn’s 24‑hour high school hackathon.">
</svelte:head>

<Bg />
<main>
    <img src="lambda-sad.png" alt="lambda frown">
    {#if status === 404}
        <h2>We couldn't find the page you requested!</h2>
        <p>Check your url and try again?</p>
        <a href="/">Go home</a>
    {:else}
        <h2><strong>{status}:</strong> {error.message}</h2>
    {/if}
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
