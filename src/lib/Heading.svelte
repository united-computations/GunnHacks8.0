<script lang="ts">
    import {fade, draw, fly} from 'svelte/transition';

    import Bg from '../lib/Bg.svelte';

    let visible = false;
    setTimeout(() => visible = true, 100)
</script>

<Bg />
<section id="heading">
    <div class="title-wrapper">
        <img src="lambda.png" alt="lambda" class="heading-image">
        {#if visible}
            <div class="title">
                {#each 'GunnHacks 8.0' as char, i}
                    <span class="title-character" in:fly="{{y: -20, delay: 1000 + i * 100, duration: 800}}">{char}</span>
                {/each}
            </div>
        {/if}
    </div>
    <hr>
    <p>The eighth iteration of GunnHacks, Gunn High School's annual hackathon organized by United Computations.</p>
</section>

<style lang="scss">
  #heading {
    text-align: center;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;

    .title-wrapper {
      display: flex;
      margin: 0 auto;
      flex-wrap: wrap;

      $heading-size: 5rem;

      .heading-image {
        height: $heading-size;
        margin: 0 auto;
      }

      .title-character {
        font-size: $heading-size;
        font-family: 'Overpass';
        letter-spacing: 0.1em;
        color: white;
        font-weight: 400;
        will-change: filter;
      }
    }
  }

  hr {
    width: 10rem;
    border: none;
    border-top: 2px solid white;
  }

  p {
    //font-size: 1.15rem;
  }
</style>
