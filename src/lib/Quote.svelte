<script lang="ts">
	import { words } from '$lib/_data';

	interface Quote {
		words: string;
		cite: string;
	}

	let quotes: Quote[] = [...words];
	let quote: Quote = quotes[Math.floor(Math.random() * quotes.length)];

	const getQuote = () => {
		const newQuotes = quotes.filter((item) => item !== quote);
		quotes = newQuotes;
		const newQuote = newQuotes[Math.floor(Math.random() * newQuotes.length)];
		quote = newQuote;

		{
			console.log(quotes);
		}
		{
			console.log(quote);
		}
	};

	{
		console.log(quotes);
	}
	{
		console.log(quote);
	}
</script>

<span class="quote-cont">
	{#if quotes.length}
		<q class="quote" title={quote.cite} cite={quote.cite}>
			{quote.words}
		</q>
		<button class="quote--button" on:click={getQuote}> new quote </button>
	{:else}
		<q
			class="quote"
			title="Jon Telles, Extremely Good & Professional Developer"
			cite="Jon Telles, Extremely Good & Professional Developer"
		>
			We're out of quotes 😔...feel free to
			<a href="mailto:jongtelles@gmail.com">email me more!</a> or{' '}
			<button class="quote--button-reset"> start over </button>
		</q>
	{/if}
</span>

<style lang="scss">
	.quote-container {
		position: relative;
		display: flex;
		flex-direction: column;
		align-items: center;
		max-width: 50%;
		margin: 0 auto;
	}

	.quote {
		background: rgba(0, 0, 0, 15%);
		border-radius: 1rem;
		font-size: 1.2rem;
		padding: 0.5rem;
		margin-top: 0.5rem;
	}

	.quote a {
		color: #eca089;
		text-decoration: none;
	}

	.quote a:hover {
		text-decoration: underline;
	}

	.quote--button {
		opacity: 0;
		visibility: hidden;
		position: absolute;
		top: -22px;
		padding: 0.5rem;
		border: 0;
		outline: 0;
		background: linear-gradient(45deg, #200d3a, #292651, #2e4770, #ce5e82, #eca089, #ecc6a2);
		color: whitesmoke;
		font-size: 1.2rem;
		font-weight: bold;
		text-transform: lowercase;
		width: 8rem;
		border-radius: 1rem;
		margin-top: 0.5rem;
		cursor: pointer;
		transition: all 0.5s ease-in-out;
	}

	.quote--button-reset {
		padding: 0.5rem;
		border: 0;
		outline: 0;
		background: linear-gradient(45deg, #200d3a, #292651, #2e4770, #ce5e82, #eca089, #ecc6a2);
		color: whitesmoke;
		font-size: 1.2rem;
		font-weight: bold;
		text-transform: lowercase;
		width: 8rem;
		border-radius: 1rem;
		cursor: pointer;
		transition: all 0.5s ease-in-out;
	}

	.quote-btn-peak,
	.quote:hover + .quote--button,
	.quote--button:hover {
		opacity: 1;
		visibility: visible;
	}
</style>
