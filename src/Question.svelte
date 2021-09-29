<script lang="ts">
    export let q: string;
    export let a: string;

    let open = false;
</script>

<div class="question-wrapper">
    <div class="question" on:click={() => open = !open}>
        <h3 class="expand">{open ? '–' : '+'}</h3>
        <h3>{@html q}</h3>
    </div>
    {#if open}
        <p>{@html a}</p>
    {/if}
</div>

<style lang="scss">
  .question-wrapper {
    margin: 0.5rem;

    .question {
      display: flex;
      cursor: pointer;

      h3 {
        margin: 0 0 0.75rem 0;
        font-size: 1.5rem;
        font-weight: normal;

        &.expand {
          margin-right: 1rem;
        }
      }
    }

    p {
      margin-top: 0;
    }
  }
</style>
