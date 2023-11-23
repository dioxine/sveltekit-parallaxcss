<section class="parallax__group">
	<slot />
</section>

<style>
	/* container around parallax layers */
	.parallax__group {
		position: relative;
		z-index: -1;
		transform-origin: center top;
		transform: scaleY(calc(1 - var(--parallax-scale)));
		margin-top: calc(
			var(--container-offset-adjustment) + (-1 * max(100vh, var(--parallax-min-height)))
		);
		margin-bottom: calc(
			-1.4 * var(--container-offset-adjustment)
		); /* -1.4 for controlling bottom */
	}
</style>
