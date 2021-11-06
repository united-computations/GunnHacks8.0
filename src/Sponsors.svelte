<script>
    import Section from './Section.svelte';
    import Sponsor from './Sponsor.svelte';
</script>

<Section title="Sponsors">
    <p>
        To sponsor our event, email us at <a href="mailto:ghshacks@gmail.com">ghshacks@gmail.com</a>.
        Find our sponsorship prospectus <a target="_blank" rel="noopener noreferrer" href="docs/sponsorship_prospectus.pdf">here</a>.
    </p>

    <div class="sponsors-content">
        <Sponsor href="https://www.wolfram.com" src="sponsors/wolfram.svg" alt="wolfram" />
    </div>
</Section>

<style lang="scss">
  .sponsors-content {
    margin: 0 auto;
    padding-top: 1rem;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    text-align: center;
  }
</style>
