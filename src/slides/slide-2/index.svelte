<script>
  import * as slides from "./slides";
</script>

<section>
	{#each Object.keys(slides) as key}
      <svelte:component this={slides[key]} />
    {/each}
</section>