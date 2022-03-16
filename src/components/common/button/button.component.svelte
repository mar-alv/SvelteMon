<script>
  export let text;
</script>

<button class={`button`}>{text}</button>

<style lang="scss">
  .button {
    border: none;
    background-color: transparent;

    &:hover {
      cursor: pointer;
    }
  }
</style>
