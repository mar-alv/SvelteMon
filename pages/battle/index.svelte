<script>
  import Modal from "@components/common/modal.component.svelte";
  import BattleButtons from "@components/battle/battleButtons.component.svelte";
  import BattleStatusCard from "@components/battle/battleStatusCard.component.svelte";

  let pokemonName = "";
  let pokemonLevel = 5;
  let pokemonMaxHP = 20;
  let pokemonActualHP = 15;
  fetch("https://pokeapi.co/api/v2/pokemon/25")
    .then((response) => response.json())
    .then((character) => {
      pokemonName = character.name.toLocaleUpperCase();
    });
</script>

<div>
  <Modal />
  <BattleStatusCard
    {pokemonName}
    {pokemonLevel}
    {pokemonMaxHP}
    {pokemonActualHP}
  />
  <BattleStatusCard
    {pokemonName}
    {pokemonLevel}
    {pokemonMaxHP}
    {pokemonActualHP}
  />

  <BattleButtons />
</div>
