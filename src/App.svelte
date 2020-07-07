<script>
  import { onMount } from "svelte";
  import Reveal from "reveal.js";
  import * as slides from "./slides";

  onMount(() => {
    let deck = new Reveal();
    deck.initialize();
  });
</script>

<main class="reveal">
  <div class="slides">
    {#each Object.keys(slides) as key}
      <svelte:component this={slides[key]} />
    {/each}
  </div>
</main>
