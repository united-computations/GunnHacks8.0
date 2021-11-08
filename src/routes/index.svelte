<script lang="ts">
    import Heading from '../lib/Heading.svelte';
    import About from '../lib/About.svelte';
    import FAQ from '../lib/FAQ.svelte';
    import Sponsors from '../lib/Sponsors.svelte';
    import Footer from '../lib/Footer.svelte';
</script>

<svelte:head>
    <title>GunnHacks 8.0</title>
    <!-- Copy pasted from 7.0; perhaps we can change? -->
    <meta name="description" content="Make, Build, Create & Learn. It’s GunnHacks 8.0, Gunn’s 24‑hour high school hackathon.">
</svelte:head>

<Heading />
<About />
<FAQ />
<Sponsors />
<Footer />

<style global lang="scss">
  body {
    background-color: rgb(17, 24, 39);
    color: white;
  }
</style>
