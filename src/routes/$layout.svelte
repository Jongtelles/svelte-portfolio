<script lang="ts">
  const time = new Date().getFullYear();
  const image = "./assets/GitHub-Mark-Light-32px.png)";
</script>

<header class="header">
  <span>
    Jon Telles<i class="fas fa-laptop-code" />Software Engineer
  </span>
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
</header>

<slot />

<footer class="footer">
  <p class="footer--copyright">
    <i class="far fa-copyright" /> Jon Telles {time}
  </p>
  <p class="footer--blurb">🙃 Made by a human being 🙃</p>
  <a
    class="gh--link"
    href="https://github.com/Jongtelles/jongtelles.github.io"
    style="background-image: url({image});"
  >
    <span>Github Link</span>
  </a>
</footer>

<style>
  .header {
    display: flex;
    align-items: center;
    padding: 0.5rem;
    color: #ffffff;
    border-bottom: 5px solid #ce5e82;
    position: static;
    top: 0;
  }

  .header span > i {
    margin: 0 5px;
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
    height: 2.5rem;
    width: 2.5rem;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
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
