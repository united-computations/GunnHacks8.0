<script>
    import Section from './Section.svelte';

    // Could also make this a nested array perhaps
    const prizes = [
        {r: '1st Overall', p: 'Gaming Mic + Wolfram Award'},
        {r: '2nd Overall', p: 'IOTunix LED Lamp + Wolfram Award'},
        {r: '3rd Overall', p: 'Amazon Echo Dot + Wolfram Award'},
        {r: '4th, 5th Overall', p: 'Discord Nitro Classic  (2 Months) + Wolfram Award'},
        {r: 'Most Creative', p: '$20 Adafruit Gift Certificate'},
        {r: 'Best Solo Hack', p: 'Discord Nitro Classic (3 Months)'},
    ];
</script>

<Section title="Prizes">
    <div class="prizes-container">
        {#each prizes as {r, p}}
            <div class="rank">{r}</div>
            <div class="prize">{p}</div>
        {/each}
    </div>
    <p>More prizes to be announced!</p>
</Section>

<style lang="scss">
  .prizes-container {
    display: grid;
    grid-template-columns: minmax(6rem, 20vw) 1fr;
    text-align: left;

    div {
      padding: 1rem 1rem 1rem 0;
      border-bottom: 1px solid #E1E1E1;

      &.prize {
        margin-left: 0.5rem;
      }
    }
  }
</style>
