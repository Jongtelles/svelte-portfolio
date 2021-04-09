<script lang="ts">
  import { onMount } from "svelte";
  import Quote from "$lib/Quote.svelte";
  import About from "$lib/About.svelte";
  import Highlight from "$lib/Highlight.svelte";
  import Project from "$lib/Project.svelte";

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
      "%c You should work with me!",
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

    setTimeout(() => {
      const icons = [...document.querySelectorAll("i")];
      icons.map((icon) => {
        return icon.classList.add("spin-cw");
      });
    }, 2000);
  });
</script>

<svelte:head>
  <meta name="description" content="Jon Telles - Software Engineer - Portfolio" />
  <!-- Facebook Meta Tags -->
  <meta property="og:url" content="https://jontell.es/" />
  <meta property="og:type" content="website" />
  <meta property="og:title" content="Jon Telles - Software Engineer - Portfolio" />
  <meta
    property="og:description"
    content="Strong communicator with a knack for mobilizing teams and translating technical concepts into plain English (or terrible Spanish)."
  />
  <meta property="og:image" content="/aboutme.png" />

  <!-- Twitter Meta Tags -->
  <meta name="twitter:card" content="summary_large_image" />
  <meta property="twitter:domain" content="jontell.es" />
  <meta property="twitter:url" content="https://jontell.es/" />
  <meta name="twitter:title" content="Jon Telles - Software Engineer - Portfolio" />
  <meta
    name="twitter:description"
    content="Strong communicator with a knack for mobilizing teams and translating technical concepts into plain English (or terrible Spanish)."
  />
  <meta name="twitter:image" content="/aboutme.png" />
  <link rel="preconnect" href="https://fonts.gstatic.com" />
  <link
    href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@300&display=swap"
    rel="stylesheet"
  />
  <script src="https://kit.fontawesome.com/cffb40c34b.js" crossorigin="anonymous"></script>
  <link rel="manifest" href="/manifest.json" />
  <title>Jon Telles: Software Engineer 💻</title>
</svelte:head>

<main>
  <Quote />
  <About />
  <h2 class="page--header">Professional Work</h2>
  <div class="flex-container flex-justify-center margin-tb-1">
    <Highlight />
  </div>
  <h2 class="page--header">Personal Projects</h2>
  <div class="flex-container flex-justify-center margin-tb-1">
    <Project />
  </div>
</main>

<style lang="scss">
  :global {
    *,
    *::after,
    *::before {
      box-sizing: border-box;
    }

    html {
      font-size: 10px;
      line-height: 1.5;
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-size: 1.6rem;
      color: whitesmoke;
      text-align: center;
    }

    h2 {
      margin: 0;
    }

    ul {
      padding: 0;
      list-style: none;
    }

    #svelte {
      background: linear-gradient(#2f9395, #65b8bf, #dd517f, #8f8cf2, #a653f5);
      background-size: cover;
      background-repeat: no-repeat;
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

    @keyframes icon-spin {
      from {
        transform: rotate(0deg);
      }
      to {
        transform: rotate(360deg);
      }
    }

    .spin-cw {
      animation-name: icon-spin;
      animation-duration: 1s;
      transition: transform 0.5s ease-in-out;
    }

    .spin-cw:hover {
      animation-name: icon-spin;
      animation-duration: 1.25s;
      animation-iteration-count: infinite;
    }
  }

  :root {
    font-family: "Noto Sans JP", sans-serif;
  }

  @media (max-width: 500px) {
    .page--header {
      font-size: 2.4rem;
    }
  }
</style>
