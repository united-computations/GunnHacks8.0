<script>
    import Section from './Section.svelte';

    const previousYears = ['7.0', '6.0', '5.0', '4.0', '3.0', '2.0', '1.0'];
</script>

<Section red>
    <div class="footer">
        <h3>Previous Years:</h3>

        <div class="footer-links">
            {#each previousYears as year}
                <a target="_blank" rel="noopener noreferrer" href={`https://${year}.gunnhacks.com`}>{year}</a>
            {/each}
        </div>
    </div>
</Section>

<style lang="scss">
  .footer {
    font-size: 1.25rem;
    display: flex;
    align-items: center;

    .footer-links {
      display: flex;
      flex-wrap: wrap;
    }

    h3 {
      margin: 0;
    }
    a {
      margin-left: 2rem;
    }
  }
</style>
