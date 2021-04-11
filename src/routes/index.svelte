<script>
	import ScrollySticky from '../components/ScrollySticky.svelte';
	import { fade } from 'svelte/transition';
</script>

<svelte:head>
	<title>Happy Birthday GNAT!!!</title>
</svelte:head>

<ScrollySticky>
	<h1>Hey there!</h1>
	<h2 transition:fade slot="sticky">
		(scroll down) <br />
		👇
	</h2>
</ScrollySticky>

<ScrollySticky>
	<h1>This is GNAT 👉</h1>
	<img transition:fade slot="sticky" alt="Gnat" src="/gnat.jpeg" class="two" >
</ScrollySticky>

<style>
	h1 {
		font-size: 2.8em;
		text-transform: uppercase;
		font-weight: 700;
	}

	h1, h2, p {
		text-align: center;
		width: 100%;
		align-self: center;
	}

	img {
		position: fixed;
		top: 0;
		right: 0;
		height: 100vh;
		width: 60vw;
	}
</style>
