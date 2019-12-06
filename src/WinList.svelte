<script>
  export let wins;
</script>

<style>
  h4 {
    color: green;
  }
</style>

<div class="grid-3">

  {#each wins as win}
    <div class="card">
      <h4 class="py-3">{win.description}</h4>
      <p>{win.createdAt.substring(0, 10)}</p>
    </div>
  {:else}
    <div class="card">Loading</div>
  {/each}

</div>
