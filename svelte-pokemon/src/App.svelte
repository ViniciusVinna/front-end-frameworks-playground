<script lang="ts">
	import { counter } from './store/counter';

	import Routes from './routes/Routes.svelte';
	import Button from './components/Button.svelte';

</script>

<h1>Meu SPA Svelte - counter: {$counter}</h1>
<Button text="Ouvi um amém?">
	Dentro do Slot

	<p slot="top">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vel fuga nihil optio commodi modi accusantium voluptas ut mollitia, officia dolore sit veniam amet, praesentium quod blanditiis sint, cumque consequatur delectus?</p>
</Button>

<Routes />
