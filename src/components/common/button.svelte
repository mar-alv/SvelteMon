<script>
  import Typography from "./typography.svelte";

  export let text;
</script>

<button class={`button`}>
  <Typography {text} />
  <!-- <img src='./rightArrow.png' alt="…" width="200" height="200"/> -->
</button>

<style lang="scss">
  .button {
    border: none;
    display: flex;
    background-color: transparent;
    strong {
      display: none;
    }

    &:hover {
      strong {
        display: initial;
      }
      cursor: pointer;
    }
  }
</style>
