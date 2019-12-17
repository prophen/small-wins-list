<script>
  import { onMount } from "svelte";
  import axios from "axios";
  import WinList from "./WinList.svelte";

  let wins = [];

  const getWins = () => {
    axios.get("https://prophen-small-wins.glitch.me/wins").then(response => {
      wins = response.data.reverse();
    });
  };
  onMount(getWins());
</script>

<div class="container">
  <h1 class="py-3">Hello Wins</h1>
  <div class="grid-3">
    <WinList {wins} />
  </div>
</div>
