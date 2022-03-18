<script>
  import Typography from "./typography.svelte";

  export let text;
</script>

<button class={`button`}>
  <Typography {text} />
</button>

<style lang="scss">
  .button {
    border: none;
    background-color: transparent;

    &:hover {
      cursor: pointer;
    }
  }
</style>
