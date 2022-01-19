<script lang="ts">
    export let red: boolean;
    export let title: string | undefined;
    export let id: string | undefined;
</script>

<section class:red {id}>
    <div class="content">
        {#if title}<h2>{title}</h2>{/if}
        <slot />
    </div>
</section>

<style lang="scss">
  section {
    font-family: 'Abel';
    background-color: white;
    color: black;
    text-align: center;

    .content {
      padding: 20px;
      margin: 0 auto;
      max-width: 1024px;

      h2 {
        text-align: center;
        font-size: 2rem;
        border-bottom: 2px solid black;
        margin-top: 0;
        margin-bottom: 1rem;
      }
    }

    &.red {
      background-color: #dd5d5c;
      color: white;

      .content h2 {
        border-bottom: 2px solid white;
      }
    }
  }
</style>
