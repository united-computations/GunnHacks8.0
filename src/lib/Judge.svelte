<script lang="ts">
    export let name: string;
    export let title: string;
    export let desc: string;
    export let src: string;
</script>

<div>
    <img {src} alt={name}>
    <h4 class="name">{name}</h4>
    <p class="desc">{desc}</p>
    <p class="title">{title}</p>
</div>

<style lang="scss">
  img {
    $size: 10rem;
    height: $size;
    width: $size;
    border-radius: 50%;
  }

  .title {
    font-style: italic;
  }

  .name {
    margin: 0.25rem 0 0.5rem;
  }

  p {
    margin: 0 0 0.25rem 0;
  }
</style>
