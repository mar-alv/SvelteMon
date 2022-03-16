<script>
  import PokemonParty ../../src/components/common/button/button.component.svelte

  let characterName;
  let list = [];

  fetch("https://pokeapi.co/api/v2/pokemon/25")
    .then((response) => response.json())
    .then((character) => {
      let p = new PokemonParty(character.name);

      list.add(p);
    });
</script>

<div>
  
</div>

