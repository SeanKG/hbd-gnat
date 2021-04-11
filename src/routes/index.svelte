<script>
	import successkid from 'images/successkid.jpg';
	import ScrollySticky from '../components/ScrollySticky.svelte';
	import { fade } from 'svelte/transition';
</script>

<svelte:head>
	<title>Happy Birthday GNAT!!!</title>
</svelte:head>

<ScrollySticky>
	<h1>Hello!!!</h1>
	<div transition:fade slot="sticky">(scroll down)</div>
</ScrollySticky>

<ScrollySticky>
	<h2>This is GNAT -></h2>
	<img transition:fade slot="sticky" alt="Gnat" src="{successkid}" class="two" >
</ScrollySticky>

<style>
	h1, h2, p {
	}

	h1 {
		font-size: 2.8em;
		text-transform: uppercase;
		font-weight: 700;
	}

	h1, h2, p {
		text-align: center;
		margin: 0 auto;
		width: 40vw;
		margin-right: 60vw;
		align-self: center;
	}

	img {
		position: fixed;
		top: 0;
		right: 0;
		height: 100vh;
		width: 60vw;
	}

	.two {
		opacity: 50%;;
	}

	@media (min-width: 480px) {
		h1 {
			font-size: 4em;
		}
	}
</style>
