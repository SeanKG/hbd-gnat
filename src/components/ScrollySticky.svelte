<script>
	import IntersectionObserver from "svelte-intersection-observer";

	let element;
	let intersecting;
</script>

<!-- <svelte:head>
	<title>Happy Birthday GNAT!!!?</title>
</svelte:head> -->

<IntersectionObserver {element} bind:intersecting threshold={1}>
	<section>
        <div bind:this={element} class="scrolly">
            <slot/>
        </div>
		{#if intersecting}
            <div class="sticky">
                <slot name="sticky" />
            </div>
		{/if}
	</section>
</IntersectionObserver>

<style>
	section {
		height: 100vh;
		width: 100vw;
		display: flex;
	}

	.scrolly {
		width: 40vw;
		margin-right: 60vw;
		vertical-align: middle;
		align-self: center;
	}

	.sticky {
		position: fixed;
		top: 0;
		right: 0;
		height: 100vh;
		width: 60vw;
	}
</style>
