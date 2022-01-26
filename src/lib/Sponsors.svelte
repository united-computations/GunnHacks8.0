<script>
    import Section from './Section.svelte';
    import Sponsor from './Sponsor.svelte';
</script>

<Section title="Sponsors" id="sponsors">
    <p>
        To sponsor our event, email us at <a href="mailto:ghshacks@gmail.com">ghshacks@gmail.com</a>.
        Find our sponsorship prospectus <a target="_blank" rel="noopener noreferrer" href="docs/sponsorship_prospectus.pdf">here</a>.
    </p>

    <div class="sponsors-content">
        <Sponsor href="https://www.wolfram.com" src="sponsors/wolfram.svg" alt="Wolfram" />
        <Sponsor href="https://gunn.paloaltopta.org/" src="sponsors/ptsa.jpeg" alt="PTSA" />
        <Sponsor href="https://linktr.ee/leadinglearners" src="sponsors/leading_learners.png" alt="Leading Learners" />
        <Sponsor href="https://1password.com/" src="sponsors/1password.svg" alt="1Password" />
        <Sponsor href="https://www.janestreet.com/" src="sponsors/jane_street.png" alt="Jane Street" />
        <Sponsor href="https://amzn.to/2GontHO" src="sponsors/iotunix.png" alt="IOTunix" />
        <Sponsor href="https://www.leangap.org/" src="sponsors/leangap.svg" alt="Leangap" />
        <Sponsor href="https://www.figma.com/" src="sponsors/figma.svg" alt="Figma" />
        <Sponsor href="https://hackp.ac/mlh-stickermule-hackathons" src="sponsors/sticker_mule.svg" alt="StickerMule" />
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
