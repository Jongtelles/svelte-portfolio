<article class="highlight">
  <h2 class="highlight--header">
    <a target="_blank" rel="noopener noreferrer" href="https://nitaac.nih.gov">NITAAC</a>
  </h2>
  <div class="highlight--img-container">
    <img
      class="highlight--img"
      alt="nitaac.nih.gov front page"
      src="https://res.cloudinary.com/ushigoroshi/image/upload/f_auto,q_auto/v1617936405/nitaac-fp_plyrdu.png"
      loading="lazy"
    />
    <img
      class="highlight--img"
      alt="nitaac.nih.gov task order page"
      src="https://res.cloudinary.com/ushigoroshi/image/upload/f_auto,q_auto/v1617936401/nitaac-task-order_erhhuw.png"
      loading="lazy"
    />
  </div>
  <p class="highlight--desc">
    Most recently, I was the lead front end developer for a refresh of the NIH Information
    Technology Acquisition and Assessment Center's public-facing website. My primary contributions
    include updating and creating markup, styles, animations, and interactions for all components
    across most-visited pages. I am also co-leading a Drupal migration, which involves refactoring
    site-wide legacy code to meet modern web standards and streamlining CMS practices.
  </p>
</article>
<article class="highlight">
  <h2 class="highlight--header">
    <a target="_blank" rel="noopener noreferrer" href="https://www.aafmaa.com">AAFMAA</a>
  </h2>
  <div class="highlight--img-container">
    <img
      class="highlight--img"
      alt="aafmaa.com front page"
      src="https://res.cloudinary.com/ushigoroshi/image/upload/f_auto,q_auto/v1617936406/aafmaa-fp_b8wmui.png"
      loading="lazy"
    />
    <img
      class="highlight--img"
      alt="aafmaa.com life insurance calculator"
      src="https://res.cloudinary.com/ushigoroshi/image/upload/f_auto,q_auto/v1617936404/aafmaa-life_hexfg3.png"
      loading="lazy"
    />
  </div>
  <p class="highlight--desc">
    I was brought on this project partway through to ensure the redesign was completed on time and
    in accordance with the high standards set by our client. My key contributions were creating
    logic, interactions, styling, and markup for dozens of components, including a highly visible
    <a href="https://www.aafmaa.com/life-insurance" target="_blank" rel="noopener noreferrer">
      life insurance calculator tool
    </a>.
  </p>
  <a
    href="http://contests.gdusa.com/gdusa-contest-winner?cc=agda19&ids=0|1250&iy=&im="
    class="highlight--award"
  >
    🏆 2019 American Graphic Design Award 🏆
  </a>
</article>
<article class="highlight">
  <h2 class="highlight--header">
    <a target="_blank" rel="noopener noreferrer" href="https://farmers.gov">Farmers.gov</a>
  </h2>
  <div class="highlight--img-container">
    <img
      class="highlight--img"
      alt="farmers.gov front page"
      src="https://res.cloudinary.com/ushigoroshi/image/upload/f_auto,q_auto/v1617936404/farmers-gov-fp_hrdl4o.png"
      loading="lazy"
    />
    <img
      class="highlight--img"
      alt="farmers.gov disaster assistance discovery tool"
      src="https://res.cloudinary.com/ushigoroshi/image/upload/f_auto,q_auto/v1617936401/farmers-gov-dadt_ysjdsv.png"
      loading="lazy"
    />
  </div>
  <p class="highlight--desc">
    Working on this high-profile government project was a great learning experience — and a
    fulfilling one as well, given its positive impact on people across the country. My core
    contributions included creating logic and functionality for the
    <a
      href="https://www.farmers.gov/recover/disaster-tool"
      target="_blank"
      rel="noopener noreferrer"
    >
      Disaster Assistance Discovery Tool
    </a>
    (which generated a significant increase in aid applications), creating and styling mobile-responsive
    pages, and updating the build process to include minification of CSS and transpilation of JS files.
  </p>
  <a
    href="http://contests.gdusa.com/gdusa-contest-winner?cc=agda18&ids=0|113817&iy=&im="
    class="highlight--award"
  >
    🏆 2018 American Graphic Design Award 🏆
  </a>
</article>

<style>
  .highlight {
    background: linear-gradient(145deg, #18363e, #2d5f6e, #2e4770, #ce5e82, #f08d7e);
    padding: 10px;
    margin: 20px;
    border-radius: 1rem;
    box-shadow: -10px 10px 10px #540d6e;
    transition: box-shadow 0.5s ease-in-out;
    border: 8px solid whitesmoke;
    max-width: 95rem;
  }

  .highlight:hover {
    box-shadow: 25px 25px 10px #2e4770;
  }

  .highlight--header a {
    color: whitesmoke;
  }

  .highlight--header a:hover {
    color: #dd517f;
  }

  .highlight--img-container {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
  }

  .highlight--img-container img {
    margin: 1rem;
    border-radius: 1rem;
    cursor: pointer;
    max-width: 35rem;
    max-height: 35rem;
    transition: transform 0.5s ease-in-out;
    transition-delay: 0.5s;
  }

  .highlight--img-container img:hover {
    transform: scale(2.2);
  }

  .highlight--desc {
    text-align: left;
  }

  .highlight--award,
  .highlight--desc a {
    color: whitesmoke;
  }

  .highlight--award:hover,
  .highlight--desc a:hover {
    color: #2e2157;
  }

  @media (max-width: 500px) {
    .highlight--img-container {
      flex-direction: column;
    }

    .highlight--img-container img {
      max-width: 27rem;
      max-height: 45rem;
    }

    .highlight--img-container img:hover {
      transform: unset;
      margin: 1rem;
    }

    .highlight--desc {
      font-size: 1.4rem;
    }

    .highlight--award {
      font-size: 1.2rem;
    }
  }
</style>
