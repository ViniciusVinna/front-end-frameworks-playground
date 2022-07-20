<script>
	import { Link } from "svelte-navigator";

	const getPokemons = fetch('https://pokeapi.co/api/v2/pokemon?limit=10')
		.then(res => res.json())
		.then(response => {
			return response.results;
		});
</script>

<style>
	.error {
		color: red;
	}
</style>

<ul>
	{#await getPokemons}
		<!-- promise is pending -->
		<p>Aguardando Pokemons...</p>
	{:then response}
		{#each response as pokemon}
			<li>
				<Link to={`/pokemon/${pokemon.name}`}>{pokemon.name}</Link>
			</li>
		{/each}
	{:catch error}
		<!-- promise was rejected -->
		<p class="error">Something went wrong: {error.message}</p>
	{/await}
</ul>
