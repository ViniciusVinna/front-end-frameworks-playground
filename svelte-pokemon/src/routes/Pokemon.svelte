<script>
	import { useParams } from "svelte-navigator";

	const params = useParams();

	const getPokemons = fetch(`https://pokeapi.co/api/v2/pokemon/${$params.id}`)
		.then(res => res.json())
</script>

	{#await getPokemons}
		<!-- promise is pending -->
		<p>Carregando {$params.id}</p>
	{:then response}
		<h1>{response.name}</h1>
		<img src={response.sprites.front_default} alt="" />
	{:catch error}
		<!-- promise was rejected -->
		<p class="error">Something went wrong: {error.message}</p>
	{/await}
