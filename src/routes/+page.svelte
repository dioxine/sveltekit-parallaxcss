<script>
	import ParallaxGroup from '$lib/components/UI/Parallax/ParallaxGroup.svelte';
	import ParallaxLayer from '$lib/components/UI/Parallax/ParallaxLayer.svelte';
</script>

<div class="header">
	<h1>Pure CSS Parallax, Y-Axis pseudo-3D</h1>
	<p>
		Parallax effect experiment #4: minimal code example inspired by <a
			href="https://keithclark.co.uk/articles/pure-css-parallax-websites/">Keith Clark</a
		>
		and <a href="https://codepen.io/hexagoncircle/pen/JjRYaZw">Ryan Mulligan</a>, explained at
		<a href="https://dev.to/ingosteinke/pure-css-parallax-perspective-beyond-landscape-images-24g2"
			>dev.to/ingosteinke/pure-css-parallax-perspective-beyond-landscape-images-24g2</a
		> using only 2D Y-axis transformations, no global body styles, no misleading clutter, and no JavaScript
		at all.
	</p>
	<p class="content">
		Side effect: preceding paragraphs must define a non-transparent background, otherwise the
		decoration will shine through. <b>Scaling:</b> this setup will upscale your content, possibly breaking
		pixel-perfect designs!
	</p>
</div>

<ParallaxGroup>
	<ParallaxLayer>
		<div class="card">
			<h1>Card 1</h1>
			<p>Slide section with cards over a perspective background</p>
			<button>BUTTON</button>
		</div>

		<div class="card">
			<h1>Card 2</h1>
			<p>Slide section with cards over a perspective background</p>
		</div>

		<div class="card">
			<h1>Card 3</h1>
			<p>Slide section with cards over a perspective background</p>
		</div>

		<div class="card">
			<h1>Card 4</h1>
			<p>Slide section with cards over a perspective background</p>
		</div>

		<div class="card">
			<h1>Card 5</h1>
			<p>Slide section with cards over a perspective background</p>
		</div>

		<div class="card">
			<h1>Card 6</h1>
			<p>Slide section with cards over a perspective background</p>
		</div>

		<div class="card">
			<h1>Card 7</h1>
			<p>Slide section with cards over a perspective background</p>
		</div>

		<div class="card">
			<h1>Card 8</h1>
			<p>Slide section with cards over a perspective background</p>
		</div>

		<div class="card">
			<h1>Card 9</h1>
			<p>Slide section with cards over a perspective background</p>
		</div>
	</ParallaxLayer>
	<!-- more layers could be added here -->
</ParallaxGroup>

<footer class="footer">
	<h1>Footer: The End</h1>
</footer>

<style>
	/* recommended other elements' opaque background etc. */

	.header,
	.footer,
	.content {
		background-color: white;
		margin: 0;
		padding: 1rem;
	}

	.header {
		position: relative;
		z-index: 1;
	}

	/* decorative styles unrelated to the parallax effect: */
	.card {
		width: 50%;
		padding: 5%;
		border: solid 1px gray;
		background: rgba(240, 230, 220, 0.9);
		margin: 0 0 7rem 1rem;
	}
</style>
