<script lang="ts">
    export let date: string;
    export let schedule: [string, string][];
</script>

<div class="schedule-column">
    <h3>{date}</h3>
    <div class="schedule-grid">
        <strong>Time</strong>
        <strong>Event</strong>

        {#each schedule as [time, name]}
            <span>{time}</span>
            <span>{name}</span>
        {/each}
    </div>
</div>

<style lang="scss">
  .schedule-column {
    width: 350px;
    flex-grow: 1;

    h3 {
      text-align: center;
      margin: 1rem 0;
      font-size: 1.33rem;
      letter-spacing: 0.025em;
    }

    .schedule-grid {
      display: grid;
      grid-template-columns: auto auto;
      text-align: left;

      > * {
        padding: 0.5rem;

        &:nth-last-child(n+3) {
          border-bottom: 1px solid rgba(255, 255, 255, 0.7);
        }
      }
    }
  }
</style>
