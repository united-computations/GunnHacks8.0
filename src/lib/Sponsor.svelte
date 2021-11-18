<script lang="ts">
    export let href: string;
    export let src: string;
    export let alt: string;
</script>

<div>
    <a target="_blank" rel="noopener noreferrer" {href}>
        <img {src} {alt}>
    </a>
</div>

<style lang="scss">
  $max-height: 5.5rem;
  $max-width: 18rem;

  div {
    flex: 1 1 $max-width;

    img {
      max-height: $max-height;
      max-width: $max-width;
      padding: 0.5rem 1rem;
    }
  }
</style>
