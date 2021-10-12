<script lang="ts">
    import {fade, draw, fly} from 'svelte/transition';

    let visible = false;
    setTimeout(() => visible = true, 100)
</script>

<div id="header-image"></div>
<section id="heading">
    {#if visible}
        <div class="title-wrapper">
            {#each 'GunnHacks 8.0' as char, i}
                <span class="title" in:fly="{{y: -20, delay: 1000 + i * 100, duration: 800}}">{char}</span>
            {/each}
        </div>
    {/if}
    <p>The eight iteration of GunnHacks, Gunn High School's annual hackathon organized by United Computations.</p>
</section>

<style lang="scss">
  #header-image {
    position: fixed;
    background-image: url('../bg.svg');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    height: 100%;
    width: 100%;
    z-index: -1;
  }

  #heading {
    text-align: center;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;

    .title-wrapper {
      .title {
        font-size: 10rem;
        transform: translate(-50%, -50%);
        font-family: 'Overpass';
        letter-spacing: 0.12em;
        color: white;
        font-weight: 400;
        will-change: filter;
      }
    }
  }
</style>
