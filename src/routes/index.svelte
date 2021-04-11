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
  <title>Jon Telles: Software Engineer 💻</title>
</svelte:head>

<main>
  <Quote />
  <About />
  <h2 class="page--header">Professional Work</h2>
  <section class="flex-container flex-justify-center margin-tb-1">
    <Highlight />
  </section>
  <h2 class="page--header">Personal Projects</h2>
  <section class="flex-container flex-justify-center margin-tb-1">
    <Project />
  </section>
</main>

<style lang="scss">
  h2 {
    margin: 0;
  }

  .flex-justify-center {
    justify-content: center;
  }

  .margin-tb-1 {
    margin: 1rem 0;
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
