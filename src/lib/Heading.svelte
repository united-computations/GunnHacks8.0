<script lang="ts">
    import {fade, draw, fly} from 'svelte/transition';
    import {InstagramIcon, FacebookIcon, MailIcon} from 'svelte-feather-icons';

    import Bg from './Bg.svelte';
    import Button from './Button.svelte';

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
    <p class="date"><strong>February 5-6, 2022</strong></p>

    <div class="buttons">
        <a href="/register"><Button>REGISTER</Button></a>
    </div>

    <div class="media-links">
        <a target="_blank" rel="noopener noreferrer" href="https://www.facebook.com/GunnHacks">
            <FacebookIcon class="icon" size="1.5x" />
        </a>
        <a target="_blank" rel="noopener noreferrer" href="https://www.instagram.com/gunn.hacks/">
            <InstagramIcon class="icon" size="1.5x" />
        </a>
        <a href="mailto:ghshacks@gmail.com">
            <MailIcon class="icon" size="1.5x" />
        </a>
    </div>

    <img class="mlh-trust-badge" src="/mlh-trust-badge-2022.svg" alt="MLH Badge 2022" />
</section>

<style lang="scss">
  #heading {
    text-align: center;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 0 20px;

    .title-wrapper {
      display: flex;
      margin: 0 auto;
      flex-wrap: wrap;
      justify-content: center;
      gap: 0.75rem;

      $heading-size: 5rem;
      $small-heading-size: 3rem;

      .heading-image {
        height: $heading-size;

        @media (max-width: 640px) {
          height: $small-heading-size;
        }
      }

      .title-character {
        font-size: $heading-size;
        font-family: 'Overpass';
        letter-spacing: 0.1em;
        color: white;
        font-weight: 400;
        will-change: filter;

        @media (max-width: 640px) {
          font-size: $small-heading-size;
        }
      }
    }
  }

  .buttons {
    margin: 1rem 0;
  }

  hr {
    width: 10rem;
    border: none;
    border-top: 2px solid white;
    margin-bottom: 1rem;
  }

  p {
    margin: 0.1rem 0;

    &.date {
      font-size: 1.25rem;
      margin-top: 1rem;
    }
  }

  .mlh-trust-badge {
    position: absolute;
    top: 0;
    right: 2rem;
    width: 7rem;

    @media (max-width: 640px) {
      width: 4rem;
      right: 1rem;
    }
  }
</style>
