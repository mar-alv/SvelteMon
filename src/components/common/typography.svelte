<script lang="ts">
  import { onMount } from "svelte";

  let container;

  export let text = "";
  export let tag = "p" as "h1" | "h2" | "h3" | "h4" | "h5" | "p" | "small";

  onMount(() => {
    const children = document.createElement(tag);
    children.textContent = text;
    container.appendChild(children);
  });
</script>

<div bind:this={container} />
