<script>
  import Button from "./common/button.component.svelte";
  let characterName;

  fetch("https://pokeapi.co/api/v2/pokemon/25")
    .then((response) => response.json())
    .then((character) => {
      characterName = character.name;
    });
</script>

{characterName}
<Button color="red" text="teste 1" />
<Button color="blue" text="teste 2" />
<Button color="green" text="teste 3" />
