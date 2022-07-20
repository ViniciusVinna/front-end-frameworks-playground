<script lang="ts">
	import TodoItem from "./TodoItem.svelte";

	export let todos: string[] = [];

	$: counter = todos.length;
</script>

<style>
	ul {
		list-style: none;
		padding: 0;
		margin: 0;
	}

	ul :global(li) {
		margin-bottom: 1rem;
		color: red;
	}
</style>

<h2>Tarefas {counter}</h2>

<ul>
	{#each todos as todo}
		<li>{todo}</li>
	{/each}
</ul>

<slot />

<p>Aqui</p>

<slot name="footer" />
