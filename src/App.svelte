<script>
	import { onMount } from 'svelte'
	import axios from 'axios'

	
	let win = ""
	$: wins = []

	
	const getWins = () => {
		axios
			.get('https://prophen-small-wins.glitch.me/wins')
			.then(response => {
				wins = response.data.reverse()
				
			})
	}
	onMount(getWins())
</script>


<style>
	h4 {
		color: green;
	}
</style>

<div class="container">
<h1 class="py-3">Hello Wins</h1>
<div class="grid-4">
{#each wins as win}
	<div class="card">
			<h4 class="py-3">{win.description}</h4>
			<p>{win.createdAt.substring(0,10)}</p>
	</div>
{/each}
</div>
</div>
