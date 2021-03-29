<script lang="ts">
	import Quote from '$lib/Quote.svelte';
	import About from '$lib/About.svelte';
</script>

<svelte:head>
	<title>Welcome</title>
</svelte:head>

<main>
	<Quote />
	<About />
</main>

<style lang="scss">
	:global {
		*,
		*::after,
		*::before {
			box-sizing: border-box;
		}

		html {
			height: 100%;
			font-size: 10px;
			line-height: 1.5;
			box-sizing: border-box;
			-webkit-text-size-adjust: 100%;
		}

		body {
			margin: 0;
			font-size: 1.6rem;
			color: whitesmoke;
			text-align: center;
			height: 100%;
			background: linear-gradient(#2f9395, #65b8bf, #dd517f, #8f8cf2, #a653f5);
			background-size: cover;
			background-repeat: no-repeat;
		}

		h2 {
			margin: 0;
		}

		ul {
			padding: 0;
			list-style: none;
		}

		/* utility */
		.flex-container {
			display: flex;
			flex-direction: row;
			flex-wrap: wrap;
		}

		.flex-container.vertical {
			flex-direction: column;
		}

		.flex-evenly {
			justify-content: space-evenly;
		}

		.flex-justify-center {
			justify-content: center;
		}

		.margin-tb-1 {
			margin: 1rem 0;
		}

		/* #svelte {
			text-align: center;
			height: 100%;
			background: linear-gradient(#2f9395, #65b8bf, #dd517f, #8f8cf2, #a653f5);
			background-size: cover;
			background-repeat: no-repeat;
		} */
	}

	:root {
		font-family: 'Noto Sans JP', sans-serif;
	}

	main {
		/* text-align: center;
		height: 100%;
		background: linear-gradient(#2f9395, #65b8bf, #dd517f, #8f8cf2, #a653f5);
		background-size: cover;
		background-repeat: no-repeat; */
	}

	h1 {
		text-transform: uppercase;
		font-size: 4rem;
		font-weight: 100;
		line-height: 1.1;
		margin: 4rem auto;
		max-width: 14rem;
	}
</style>
