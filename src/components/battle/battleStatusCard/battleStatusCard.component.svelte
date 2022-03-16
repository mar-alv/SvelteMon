<script>
  export let pokemonName = "";
  export let pokemonLevel = 0;
  export let pokemonMaxHP = 0;
  export let pokemonActualHP = 0;
</script>

<div class="battleStatusCard">
  {pokemonName}
  Lv{pokemonLevel}
  {pokemonActualHP}/
  {pokemonMaxHP}
</div>

<style>
</style>
