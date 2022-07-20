<script lang="ts">
	import { counter } from '../store/counter';

	export let text = "";

	function increment() {
		$counter++;
	}
</script>

<style>
	button {
		background-color: #4CAF50;
		color: white;
		padding: 14px 20px;
		margin: 8px 0;
		border: none;
		cursor: pointer;
		width: 100%;
	}
</style>

<slot name="top" />

<button on:click|preventDefault={increment}>{text} - {$counter}</button>

<slot />

<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. In animi quis saepe laboriosam quod mollitia quisquam dolore, illo ut deleniti quidem reiciendis totam modi distinctio dicta sunt illum! Quod, deleniti.</p>
