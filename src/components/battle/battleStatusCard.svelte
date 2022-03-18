<script>
  export let pokemonName = "";
  export let pokemonLevel = 0;
  export let pokemonMaxHP = 0;
  export let pokemonActualHP = 0;
</script>

<div class="battleStatusCard">
  <div class="battleStatusCard__body">
    <div>
      {pokemonName}
      Lv{pokemonLevel}
    </div>
    <div>HP</div>
    <div>
      {pokemonActualHP}/
      {pokemonMaxHP}
    </div>
  </div>
</div>

<style lang="scss">
  .battleStatusCard {
    border-radius: 5px;
    border: 5px solid black;

    &__body {
      padding: 5px;
    }
  }
</style>
