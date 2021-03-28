<script lang="ts">
	import Quote from '$lib/Quote.svelte';
</script>

<svelte:head>
	<title>Welcome</title>
</svelte:head>

<main>
	<h1>Hello world!</h1>

	<Quote />

	<p>Visit <a href="https://svelte.dev">svelte.dev</a> to learn how to build Svelte apps.</p>
</main>

<style lang="scss">
	:root {
		font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell,
			'Open Sans', 'Helvetica Neue', sans-serif;
	}

	main {
		text-align: center;
		height: 100%;
		background: linear-gradient(#2f9395, #65b8bf, #dd517f, #8f8cf2, #a653f5);
		background-size: cover;
		background-repeat: no-repeat;
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		width: 100%;
		display: flex;
		flex-direction: column;
	}

	h1 {
		text-transform: uppercase;
		font-size: 4rem;
		font-weight: 100;
		line-height: 1.1;
		margin: 4rem auto;
		max-width: 14rem;
	}

	p {
		max-width: 14rem;
		margin: 2rem auto;
		line-height: 1.35;
	}

	@media (min-width: 480px) {
		h1 {
			max-width: none;
		}

		p {
			max-width: none;
		}
	}
</style>
