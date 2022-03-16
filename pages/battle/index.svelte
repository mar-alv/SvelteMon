<script>
  import BattleButtons from "../../src/components/battle/battleButtons/battleButtons.component.svelte";
  import BattleNarration from "../../src/components/battle/battleNarration/battleNarration.component.svelte";
  import BattleStatusCard from "../../src/components/battle/battleStatusCard/battleStatusCard.component.svelte";

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
  <BattleNarration {pokemonName} />
  <BattleButtons />
</div>
