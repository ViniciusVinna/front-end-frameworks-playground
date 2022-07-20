<script>
	import { Router, Link, Route } from "svelte-navigator";

	import Pokemons from "../components/Pokemons.svelte";
	import About from './About.svelte';
	import Pokemon from './Pokemon.svelte';
</script>

<Router>
	<nav>
		<Link to="/">Home</Link>
		<Link to="about">About</Link>
		<Link to="blog">Blog</Link>
	</nav>

	<div>
		<Route path="/" component={Pokemons} />
		<Route path="about" component={About} />
		<Route path="pokemon/:id" component={Pokemon} />
	</div>
</Router>
