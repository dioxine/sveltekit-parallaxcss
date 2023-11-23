<div class="parallax__layer parallax__layer--background" />
<div class="parallax__layer parallax__layer--foreground">
	<slot />
</div>

<style>
	.parallax__layer {
		transform-origin: center top;
		transform: scaleY(calc(1 / (1 - var(--parallax-scale))));
	}

	.parallax__layer--foreground {
		position: relative;
		top: 0;
	}

	.parallax__layer--background {
		position: sticky;
		z-index: -2;
		top: 0;
		height: 100%;
		min-height: 100vh;
		min-height: max(100vh, var(--parallax-min-height));
		background-attachment: fixed; /* legacy browser fallback */
		/* decorative styles unrelated to the parallax effect: */
		background-repeat: repeat;
		background-size: 10%;
		background-image: url("data:image/svg+xml,%3Csvg width='40' height='40' viewBox='0 0 40 40' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Ccircle cx='20' cy='20' r='18' stroke='none' fill='skyblue'/%3E%3C/svg%3E");
	}

	/* hide imperfect endings behind a gradient */
	.parallax__layer--background::before {
		content: '';
		display: block;
		position: absolute;
		top: 0;
		height: max(100vh, var(--parallax-min-height));
		width: 100%;
		background: linear-gradient(rgba(255, 255, 255, 1) 0%, rgba(255, 255, 255, 0) 100%);
	}
	.parallax__layer--background::after {
		content: '';
		display: block;
		position: absolute;
		bottom: 0;
		height: 4rem;
		width: 100%;
		background: linear-gradient(rgba(255, 255, 255, 0) 0%, rgba(255, 255, 255, 1) 100%);
	}
</style>
