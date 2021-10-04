<script lang="ts">
    import {fade, draw, fly} from 'svelte/transition';

    import About from './About.svelte';
    import FAQ from './FAQ.svelte';

    let visible = false;

    setTimeout(() => visible = true, 100)
</script>

<section id="about">
    {#if visible}
        <div class="title-wrapper">
            {#each 'GunnHacks 8.0' as char, i}
                <span class="title" in:fly="{{y: -20, delay: 1000 + i * 100, duration: 800}}">{char}</span>
            {/each}
        </div>
    {/if}
    <p>The eight iteration of GunnHacks, Gunn High School's annual hackathon organized by United Computations.</p>
</section>

<About />
<FAQ />

<link href="https://fonts.googleapis.com/css?family=Overpass:100,400" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Abel&display=swap" rel="stylesheet">

<style lang="scss">
  :global(body) {
    background-color: rgb(17, 24, 39);
    color: white;
  }

  #about {
    text-align: center;

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
