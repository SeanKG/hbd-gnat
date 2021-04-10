<script>
	import successkid from 'images/successkid.jpg';

	import IntersectionObserver from "svelte-intersection-observer";

	let element;
	let intersecting;
</script>


<svelte:head>
	<title>Happy Birthday GNAT!!!?</title>
</svelte:head>

<IntersectionObserver {element} bind:intersecting threshold={1}>
	<section>
		<h1 bind:this={element}>Hello!!!</h1>
		{#if intersecting}
			<img alt="Hey" src="{successkid}">
		{/if}
	</section>
</IntersectionObserver>

<section>
	<h2>This is GNAT -></h2>
	<img alt="Gnat" src="{successkid}" class="two">
</section>

<style>
	h1, figure, p {
		text-align: center;
		margin: 0 auto;
	}

	h1 {
		font-size: 2.8em;
		text-transform: uppercase;
		font-weight: 700;
		/* margin: 0 0 0.5em 0; */
	}

	figure {
		margin: 0 0 1em 0;
	}

	/* img {
		width: 100%;
		max-width: 400px;
		margin: 0 0 1em 0;
	} */

	p {
		/* margin: 1em auto; */
	}

	section {
		height: 100vh;
		width: 100vw;
		display: flex;
	}

	h1, h2, p {
		/* height: 100vh; */
		width: 40vw;
		margin-right: 60vw;
		/* margin: auto 60vw auto 0; */
		vertical-align: middle;
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
