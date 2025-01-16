<script lang="ts">
	import '../app.css';
	import PageEnd from '../components/page-end.svelte';

	let { children } = $props();
</script>

<div class="app">

	<main>
		{@render children()}
	</main>

	<footer>
		<div class="flex flex-row items-center w-screen pl-2 pr-2">
			<svg width="40px" height="40px" viewBox="0 0 48 48" xmlns="http://www.w3.org/2000/svg">
				<defs>
				  <style>.c{fill:none;stroke:#7D359C;stroke-linecap:round;stroke-linejoin:round;}</style>
				</defs>
				<!-- Add rx and ry to the <rect> to round the corners -->
				<rect width="48" height="48" fill="black" rx="24" ry="24"/>
				<g id="a" transform="rotate(0, 24, 24)">
				  <polyline class="c" points="32.1313 11.85 24 36.15 15.8687 11.85"/>
				</g>
				<g id="b"></g>
			</svg>
			<PageEnd />
			<svg width="40px" height="40px" viewBox="0 0 48 48" xmlns="http://www.w3.org/2000/svg">
				<defs>
				  <style>.c{fill:none;stroke:#7D359C;stroke-linecap:round;stroke-linejoin:round;}</style>
				</defs>
				<!-- Add rx and ry to the <rect> to round the corners -->
				<rect width="48" height="48" fill="black" rx="24" ry="24"/>
				<g id="a" transform="rotate(0, 24, 24)">
				  <polyline class="c" points="32.1313 11.85 24 36.15 15.8687 11.85"/>
				</g>
				<g id="b"></g>
			</svg>
		</div>
	</footer>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
