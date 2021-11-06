<script>
    import Section from './Section.svelte';

    const previousYears = ['7.0', '6.0', '5.0', '4.0', '3.0', '2.0'];
</script>

<Section red>
    <div class="footer">
        <h3>Previous Years:</h3>

        {#each previousYears as year}
            <a target="_blank" rel="noopener noreferrer" href={`GunnHacks${year}`}>{year}</a>
        {/each}
        <!-- 1.0 is special and has the URL "/gunnhacks" instead of "/GunnHacks1.0" -->
        <a target="_blank" rel="noopener noreferrer" href="/gunnhacks">1.0</a>
    </div>
</Section>

<style lang="scss">
  .footer {
    font-size: 1.25rem;
    display: flex;
    align-items: center;

    h3 {
      margin: 0;
    }
    a {
      margin-left: 2rem;
    }
  }
</style>
