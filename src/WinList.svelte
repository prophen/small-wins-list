<script>
  import Card from "./Card.svelte";
  import WinCard from "./WinCard.svelte";
  export let wins;
</script>

<div class="grid-3">

  {#each wins as win}
    <WinCard {win} />
  {:else}
    <Card>Loading</Card>
  {/each}

</div>
