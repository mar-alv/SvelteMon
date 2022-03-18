<script>
  import Button from "@components/common/button.svelte";
</script>

<div class="battleButtons">
  <div class="battleButtons__row">
    <Button text="FIGHT" />
    <Button text="BAG" />
  </div>
  <div class="battleButtons__row">
    <Button text="POKÉMON" />
    <Button text="RUN" />
  </div>
</div>

<style lang="scss">
  .battleButtons {
    display: grid;
    grid-row: auto auto;
    grid-template-columns: 100px 100px;
  }
</style>
