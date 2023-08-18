<script>
	import { onMount } from 'svelte';
	import { browser } from '$app/environment';
	import { createScene } from '$lib/scene.js';

	let el;
	if (browser) {
		onMount(() => {
			console.log('el 3', el);
			createScene(el);
		});
	}
</script>

<p>Canvas:</p>

<canvas bind:this={el} />

<p>Hello</p>

<style>
	canvas {
		width: 80%;
		height: 80%;
		border: 1px solid black;
	}
</style>
