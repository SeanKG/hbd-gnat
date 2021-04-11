<script>
	import ScrollySticky from '../components/ScrollySticky.svelte';
	import Confetti from '../components/Confetti.svelte';
	import { fade, fly } from 'svelte/transition';
</script>

<svelte:head>
	<title>Happy Birthday GNAT!!!</title>
</svelte:head>

<ScrollySticky>
	<h1>Hey there!</h1>
	<h2 out:fade slot="sticky">
		(scroll down) <br />
		👇
	</h2>
</ScrollySticky>

<ScrollySticky>
	<h1>This is GNAT 👉</h1>
	<div slot="sticky" in:fade class="gnat-contain sticky">
		<img  alt="Gnat" src="/gnat.jpeg" class="gnat"/>
	</div>
</ScrollySticky>

<ScrollySticky>
	<h1>Gnat is pretty cool</h1>
	<div slot="sticky" class="gnat-contain sticky">
		<img  alt="Gnat" src="/gnat.jpeg" class="gnat"/>
		<img alt="sunglasses" 
			src="/sunglasses2.png" 
			class="sunglasses" 
			in:fly="{{ x: 200, duration: 1000 }}"
			out:fade
		/>
	</div>
</ScrollySticky>

<ScrollySticky>
	<h1>
		Also today is Gnat's Birthday!
		<br />
		<small>(April 11)</small>
	</h1>
	<div slot="sticky" class="gnat-contain sticky">
		<img  alt="Gnat" src="/gnat.jpeg" class="gnat"/>
		<img alt="sunglasses" src="/sunglasses2.png" class="sunglasses top"/>
		<img alt="birthday hat" src="/birthday-hat.png" class="hat" in:fly="{{ y: -300, duration: 1000}}"/>
	</div>
</ScrollySticky>

<ScrollySticky>
	<h1>So I made this dumb webiste to wish her a happy birthday 💻</h1>
	<div slot="sticky" class="gnat-contain sticky">
		<img  alt="Gnat" src="/gnat.jpeg" class="gnat"/>
		<img alt="sunglasses" src="/sunglasses2.png" class="sunglasses top"/>
		<img alt="birthday hat" src="/birthday-hat.png" class="hat"/>
	</div>
</ScrollySticky>

<ScrollySticky>
	<h1>Happy Birthday Gnat!!! <br />🎉🎉🎉</h1>
	<div slot="sticky" class="sticky">
		<div class="gnat-contain">
			<img alt="Gnat" src="/gnat.jpeg" class="gnat"/>
			<img alt="sunglasses" src="/sunglasses2.png" class="sunglasses top"/>
			<img alt="birthday hat" src="/birthday-hat.png" class="hat"/>
		</div>
		<div class="confetti">
			<Confetti />
		</div>
	</div>
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
		z-index: 110;
		position: relative;
	}

	.sticky {
		display: flex;
		margin: auto;
		z-index: 100;
	}

	.gnat-contain {
		width: 631px;
		height: 631px;
		position: relative;
	}

	.gnat {
		display: block;
		width: auto;
		height: auto;
		margin: auto;
		border-radius: 50%;
	}

	.sunglasses {
		position: absolute;
		width: 230px;
		top: 162px;
		left: 211px;
	}

	.hat {
		position: absolute;
		width: 200px;
		top: -146px;
		left: 226px;
		height: 217px;
	}

	.top {
		z-index: 99;
	}

	.confetti {
		position: fixed;
		top: 0;
		right: 0;
		bottom: 0;
		left: 0;
		z-index: 120;
	}

	@media screen and (max-width: 450px) {
		.gnat-contain {
		    transform: scale(0.5) translateX(-335px);
		}
	}
</style>
