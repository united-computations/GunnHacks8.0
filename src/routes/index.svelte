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
  // Style svg icons in <Heading>
  // Component scoped css forces my hand here, but hopefully there is a cleaner way to do this
  .icon {
    margin: 0 0.5rem;
  }
</style>
