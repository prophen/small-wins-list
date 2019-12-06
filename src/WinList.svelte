<script>
  import Card from "./Card.svelte";
  export let wins;
</script>

<div class="grid-3">

  {#each wins as win}
    <Card>
      <h4 class="py-3">{win.description}</h4>
      <p>{win.createdAt.substring(0, 10)}</p>
    </Card>
  {:else}
    <Card>Loading</Card>
  {/each}

</div>
