<script lang="ts">
  import { onMount } from "svelte";
  import { words } from "$lib/_data";

  let quoteBtnPeek = false;
  let quotes = [...words];
  let quote = quotes[Math.floor(Math.random() * quotes.length)];

  const getQuote = () => {
    quotes = quotes.filter((item) => item !== quote);
    quote = quotes[Math.floor(Math.random() * quotes.length)];
  };

  onMount(() => {
	  console.log("this is just a log to make sure the onmount is only happening once...")
    setTimeout(() => {
      quoteBtnPeek = true;
    }, 500);

    setTimeout(() => {
      quoteBtnPeek = false;
    }, 2000);
  });
</script>

<span class="quote-container">
  {#if quotes.length}
    <q class="quote" title={quote.cite} cite={quote.cite}>
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
    >
      We're out of quotes 😔...feel free to
      <a href="mailto:jongtelles@gmail.com">email me more!</a> or{" "}
      <button
        class="quote--button-reset"
        on:click={() => {
          quotes = [...words];
          quote = quotes[Math.floor(Math.random() * quotes.length)];
        }}
      >
        start over
      </button>
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

    .quote {
      background: rgba(0, 0, 0, 15%);
      border-radius: 1rem;
      font-size: 1.2rem;
      padding: 0.5rem;
      margin-top: 0.5rem;

      a {
        color: #eca089;
        text-decoration: none;

        &:hover {
          text-decoration: underline;
        }
      }

      &:hover {
        + .quote--button {
          opacity: 1;
          visibility: visible;
        }
      }
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

      &:hover {
        opacity: 1;
        visibility: visible;
      }
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
  }
</style>
