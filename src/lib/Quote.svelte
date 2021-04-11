<script lang="ts">
  import { onMount } from "svelte";
  import { words } from "$lib/_data";

  const initialQuotes = [...words];
  const initialQuote = words[Math.floor(Math.random() * initialQuotes.length)];
  let quoteBtnPeek = false;
  let quotes;
  let quote;

  const getQuote = () => {
    quotes = quotes.filter((item) => item !== quote);
    quote = quotes[Math.floor(Math.random() * quotes.length)];
  };

  const resetQuotes = () => {
    quotes = initialQuotes;
    quote = quotes[Math.floor(Math.random() * quotes.length)];
  };

  onMount(() => {
    quotes = initialQuotes;
    quote = initialQuote;
    setTimeout(() => {
      quoteBtnPeek = true;
    }, 500);

    setTimeout(() => {
      quoteBtnPeek = false;
    }, 2000);
  });
</script>

<span class="quote-container">
  {#if !quotes}
    <p class="quote" style="background-color: rgba(0, 0, 0, 20%);">loading...</p>
  {:else if quotes && quotes.length}
    <q
      class="quote"
      title={quote.cite}
      cite={quote.cite}
      style="background-color: rgba(0, 0, 0, 20%);"
    >
      {quote.words}
    </q>
    <button
      class={quoteBtnPeek ? "quote-btn-peek quote--button" : "quote--button"}
      on:click={getQuote}
    >
      new quote
    </button>
  {:else}
    <q
      class="quote"
      title="Jon Telles, Extremely Good & Professional Developer"
      cite="Jon Telles, Extremely Good & Professional Developer"
      style="background-color: rgba(0, 0, 0, 20%);"
    >
      We're out of quotes 😔...feel free to
      <a href="mailto:jongtelles@gmail.com">email me more!</a> or
      <button class="quote--button-reset" on:click={resetQuotes}> start over </button>
    </q>
  {/if}
</span>

<style>
  .quote-container {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 50%;
    margin: 0 auto;
  }

  .quote {
    border-radius: 1rem;
    font-size: 1.2rem;
    padding: 0.5rem;
    margin-top: 1rem;
  }

  .quote:hover + .quote--button {
    opacity: 1;
    visibility: visible;
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

  .quote--button:hover {
    opacity: 1;
    visibility: visible;
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
  }

  .quote-btn-peek {
    opacity: 1;
    visibility: visible;
  }

  @media (max-width: 500px) {
    .quote-container {
      margin: 20px auto;
      max-width: 95%;
    }

    .quote--button {
      opacity: 1;
      visibility: visible;
    }
  }
</style>
