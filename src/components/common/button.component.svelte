<script>
    export let text=''
    export let color=''
</script>

<button class={`button button--${color}`}>{text}</button>

<style lang="scss">
  .button {
    border: 1px black solid;

    &--red {
      background-color: red;
    }

    &--blue {
      background-color: blue;
    }

    &--green {
      background-color: green;
    }
  }
</style>
