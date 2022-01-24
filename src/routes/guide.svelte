<script lang="ts">
    import {ArrowLeftIcon} from 'svelte-feather-icons';
    import Bg from '../lib/Bg.svelte';
</script>

<svelte:head>
    <title>Hacker's Guide | GunnHacks 8.0</title>
    <meta name="description" content="Make, Build, Create & Learn. It’s GunnHacks 8.0, Gunn’s 24‑hour high school hackathon.">
</svelte:head>

<Bg/>
<a href="/"><ArrowLeftIcon size="1x" /><span>Back to home</span></a>
<iframe src="https://docs.google.com/document/d/e/2PACX-1vRAglw1mef3nzTTRTkP1eVDH6Tpt6kEZUz0lgrWJCm68tFDHNLM-GIDUpZUZkXEIF5FqUtjunfUNfKY/pub?embedded=true"
        frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>

<style lang="scss">
  iframe {
    // The position: fixed and z-index wasn't needed last year, but for whatever reason is this time around
    position: fixed;
    width: 100%;
    height: 100%;
    margin: 0 auto;
  }

  a {
    position: absolute;
    top: 1rem;
    left: 1rem;
    z-index: 2;
    text-decoration: none;
    display: flex;
    align-items: center;

    span {
      margin-left: 0.75rem;
    }
  }
</style>
