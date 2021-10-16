<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<style>
	main {
		position: relative;
		background-color: #2b3531;
		margin: 0 auto;
		box-sizing: border-box;
		padding: 2em;
		max-width: 56em;
	}
</style>

<Nav {segment}/>

<main>
	<slot></slot>
</main>