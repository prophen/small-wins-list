<script>
  import Card from "./Card.svelte";
  export let win;
</script>

<Card>
  <h4 class="py-3">{win.description}</h4>
  <p>{win.createdAt.substring(0, 10)}</p>
</Card>
