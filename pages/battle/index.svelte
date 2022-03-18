<script>
  import Modal from "@components/common/modal.svelte";
  import Button from "@components/common/button.svelte";
  import BattleButtons from "@components/battle/battleButtons.svelte";
  import BattleStatusCard from "@components/battle/battleStatusCard.svelte";

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

<div class="battlePage">
  <Modal position="bottom">
    What will {pokemonName} do?
  </Modal>
  <Modal position="right">
    <BattleButtons />
  </Modal>

  <BattleStatusCard
    {pokemonName}
    {pokemonLevel}
    {pokemonMaxHP}
    {pokemonActualHP}
  />
  <Button text="aaaa" />

  <BattleStatusCard
    {pokemonName}
    {pokemonLevel}
    {pokemonMaxHP}
    {pokemonActualHP}
  />
</div>

<style lang="scss">
  .battlePage {
    position: relative;
  }
</style>
