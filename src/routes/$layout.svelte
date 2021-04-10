<script lang="ts">
  import { onMount } from "svelte";
  const time = new Date().getFullYear();
  let canvas: HTMLCanvasElement;

  onMount(() => {
    const ctx = canvas.getContext("2d");
    let frame;

    (function loop() {
      frame = requestAnimationFrame(loop);

      const imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);

      for (let p = 0; p < imageData.data.length; p += 4) {
        const i = p / 4;
        const x = i % canvas.width;
        const y = (i / canvas.height) >>> 0;

        const t = window.performance.now();

        const r = 64 + (128 * x) / canvas.width + 64 * Math.sin(t / 1000);
        const g = 64 + (128 * y) / canvas.height + 64 * Math.cos(t / 1400);
        const b = 128;

        imageData.data[p + 0] = r;
        imageData.data[p + 1] = g;
        imageData.data[p + 2] = b;
        imageData.data[p + 3] = 255;
      }

      ctx.putImageData(imageData, 0, 0);
    })();

    return () => {
      cancelAnimationFrame(frame);
    };
  });
</script>

<header class="header">
  <a href="/" class="header--link">
    Jon Telles<i class="fas fa-laptop-code" />Software Engineer
  </a>
  <ul class="header--links">
    <li class="header--item">
      <a
        class="header--link"
        href="https://drive.google.com/file/d/1VnTYC66Y8r_pYYQjSIlAy2Bkaw-uZ91B/view?usp=sharing"
        target="_blank"
        rel="noopener noreferrer"
        aria-label="my resume"
      >
        <i class="far fa-file-alt" title="my resume" />Resume
      </a>
    </li>
    <li class="header--item">
      <a
        class="header--link"
        href="https://www.linkedin.com/in/jongtelles/"
        target="_blank"
        rel="noopener noreferrer"
        aria-label="my linkedin account"
      >
        <i class="fab fa-linkedin" title="my linkedin account" />
        LinkedIn
      </a>
    </li>
    <li class="header--item">
      <a
        class="header--link"
        href="https://github.com/Jongtelles"
        target="_blank"
        rel="noopener noreferrer"
        aria-label="my github account"
      >
        <i class="fab fa-github" title="my github account" />Github
      </a>
    </li>
    <li class="header--item">
      <a class="header--link" href="mailto:jongtelles@gmail.com" aria-label="email me">
        <i class="far fa-envelope" title="email me" />Email
      </a>
    </li>
  </ul>
  <a class="header--link" href="/experiments">
    <i class="fas fa-flask" title="experiments" />Experiments
  </a>
</header>

<slot />

<footer class="footer">
  <p class="footer--copyright">
    <i class="far fa-copyright" /> Jon Telles {time}
  </p>
  <p class="footer--blurb">🙃 Made by a human being 🙃</p>
  <a class="gh--link" href="https://github.com/Jongtelles/svelte-portfolio">
    <span>Github link</span>
    <div class="canvas-container"><canvas bind:this={canvas} width={32} height={32} /></div>
  </a>
</footer>

<style>
  :global(#svelte) {
    background: linear-gradient(#2f9395, #65b8bf, #dd517f, #8f8cf2, #a653f5);
    background-size: cover;
    background-repeat: no-repeat;
  }

  :global(*, *::after, *::before) {
    box-sizing: border-box;
  }

  :global(html) {
    font-size: 10px;
    line-height: 1.5;
    box-sizing: border-box;
  }

  :global(body) {
    margin: 0;
    font-size: 1.6rem;
    color: whitesmoke;
    text-align: center;
  }

  :global(ul) {
    padding: 0;
    list-style: none;
  }

  /* utility */
  :global(.flex-container) {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }

  :global(.spin-cw) {
    animation-name: icon-spin;
    animation-duration: 1s;
    transition: transform 0.5s ease-in-out;
  }

  .header {
    display: flex;
    align-items: center;
    padding: 0.5rem 1rem;
    color: #ffffff;
    border-bottom: 5px solid #ce5e82;
    position: static;
    top: 0;
  }

  .header--links {
    display: flex;
    flex-direction: row;
    margin-left: auto;
  }

  .header--item {
    color: white;
  }

  .header--link {
    color: white;
    padding: 0.5rem;
  }

  .header--link:hover {
    color: #dd517f;
  }

  .header--link i {
    margin-right: 0.5rem;
  }

  .header--link i:first-of-type {
    margin: 0 0.5rem;
  }

  .footer {
    padding: 0.75rem;
    min-height: 2.5rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: static;
    bottom: 0;
  }

  .footer--blurb {
    margin: 0.75rem 0;
    font-size: 1rem;
  }

  .footer--copyright {
    margin: 0.5rem 0 0;
    font-size: 1.2rem;
  }

  .footer i {
    margin-right: 0.5rem;
  }

  .gh--link {
    height: 3.2rem;
    width: 3.2rem;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
  }

  canvas {
    width: 32px;
    height: 32px;
    background-color: #666;
    -webkit-mask: url(./assets/github-logo.png) 50% 50% no-repeat;
    mask: url(./assets/github-logo.png) 50% 50% no-repeat;
  }

  .gh--link span {
    position: absolute;
    left: -10000px;
    top: auto;
    width: 1px;
    height: 1px;
    overflow: hidden;
  }

  @media (max-width: 500px) {
    .header {
      flex-direction: column;
    }

    .header--links {
      margin: 0.5rem 0;
    }
  }
</style>
