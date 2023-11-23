<script>
	import '../global.css';
</script>

<slot />

<style>

	:root {
		--parallax-scale: 0.1; /* pseudo-perspective depth, 0=deactivate */
		--parallax-min-height: 0rem; /* could be overwritten by JS measurement if too low */
		--container-offset-adjustment: 10rem;
	}

	/* disable if requested for accessibility reasons */
	@media (prefers-reduced-motion) {
		:root {
			--parallax-scale: 0;
		}
	}
</style>
