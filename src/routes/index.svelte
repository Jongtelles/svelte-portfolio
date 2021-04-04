<script lang="ts">
  import { onMount } from "svelte";
  import Quote from "$lib/Quote.svelte";
  import About from "$lib/About.svelte";

  onMount(() => {
    console.log(
      "%c Welcome to my porfolio!",
      "font-weight: bold; font-size: 40px;color: rgb(32,13,58); text-shadow: 3px 3px 0 rgb(166,33,106) , 6px 6px 0 rgb(236,28,75) , 9px 9px 0 rgb(241,106,67) , 12px 12px 0 rgb(247,217,105) , 15px 15px 0 rgb(2,135,206) , 18px 18px 0 rgb(47,147,149)"
    );
    console.log(
      "%c Enjoy your stay!",
      "font-weight: bold; font-size: 40px;color: rgb(32,13,58); text-shadow: 3px 3px 0 rgb(166,33,106) , 6px 6px 0 rgb(236,28,75) , 9px 9px 0 rgb(241,106,67) , 12px 12px 0 rgb(247,217,105) , 15px 15px 0 rgb(2,135,206) , 18px 18px 0 rgb(47,147,149)"
    );
    console.log(
      "%c You should hire me!",
      "font-weight: bold; font-size: 40px;color: rgb(32,13,58); text-shadow: 3px 3px 0 rgb(166,33,106) , 6px 6px 0 rgb(236,28,75) , 9px 9px 0 rgb(241,106,67) , 12px 12px 0 rgb(247,217,105) , 15px 15px 0 rgb(2,135,206) , 18px 18px 0 rgb(47,147,149)"
    );
    console.log(
      "%c I'm fun to work with",
      "font-weight: bold; font-size: 40px;color: rgb(32,13,58); text-shadow: 3px 3px 0 rgb(166,33,106) , 6px 6px 0 rgb(236,28,75) , 9px 9px 0 rgb(241,106,67) , 12px 12px 0 rgb(247,217,105) , 15px 15px 0 rgb(2,135,206) , 18px 18px 0 rgb(47,147,149)"
    );
    console.log(
      "%c and good at my job!",
      "font-weight: bold; font-size: 40px;color: rgb(32,13,58); text-shadow: 3px 3px 0 rgb(166,33,106) , 6px 6px 0 rgb(236,28,75) , 9px 9px 0 rgb(241,106,67) , 12px 12px 0 rgb(247,217,105) , 15px 15px 0 rgb(2,135,206) , 18px 18px 0 rgb(47,147,149)"
    );
  });
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
  }

  :root {
    font-family: "Noto Sans JP", sans-serif;
  }

  /* h1 {
		text-transform: uppercase;
		font-size: 4rem;
		font-weight: 100;
		line-height: 1.1;
		margin: 4rem auto;
		max-width: 14rem;
	} */
</style>
