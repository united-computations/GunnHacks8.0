<script>
    import Section from './Section.svelte';

    // Could also make this a nested array perhaps
    const prizes = [
        {r: '1st Overall', p: 'Gaming Mouse + Wolfram Award + Leading Learners Expansion Pack + Student Makers Award'},
        {r: '2nd Overall', p: 'IOTunix LED Lamp + Wolfram Award + Leading Learners Expansion Pack + Student Makers Award'},
        {r: '3rd Overall', p: 'Amazon Echo Dot + Wolfram Award + Leading Learners Expansion Pack'},
        {r: '4th, 5th Overall', p: 'Discord Nitro Classic  (2 Months) + Wolfram Award'},
        {r: 'Most Creative', p: '$20 Adafruit Gift Certificate'},
        {r: 'Best Solo Hack', p: 'Discord Nitro Classic (3 Months) + Leading Learners Expansion Pack'},
        {r: 'Best All-Girls Team', p: 'Anker SoundCore Bluetooth Speaker'},
        {r: 'Best UI/UX Design', p: '$50 Figma Store Gift Card'},
        {r: 'Best Domain Registered with Domain.com', p: 'PowerSquare Qi Wireless Phone Charger'},
        {r: 'Best Hardware Hack Sponsored by Digi-Key', p: 'Grove Beginner Kit'},
        {r: 'Most Creative Use of Twilio', p: 'Twilio Swag Box, GameGo Console'},
        {r: 'Best Web Monetization Project', p: 'Portable Charger, Coil Pin & $60 Credit'},
        {r: 'Best Use of Auth0', p: 'Exclusive Auth0 Swag (Branded Tumbler, Rubik\'s Cube & Sticker)'},
    ];
</script>

<Section title="Prizes" id="prizes">
    <div class="prizes-container">
        {#each prizes as {r, p}}
            <div class="rank">{r}</div>
            <div class="prize">{p}</div>
        {/each}
    </div>
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
