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
		<p>Aguardando Pokemons...</p>

	{:then response}
		{#each response as {name}, index}
			<li>
				<Link to={`/pokemon/${name}`}>{name} - {index}</Link>
			</li>
		{/each}
	{:catch error}
		<!-- promise was rejected -->
		<p class="error">Something went wrong: {error.message}</p>
	{/await}
</ul>
