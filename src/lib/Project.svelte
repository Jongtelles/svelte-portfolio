<article class="project">
  <div>
    <i class="las la-link" />
    <a
      href="https://game-of-life-viz.netlify.app/"
      target="_blank"
      rel="noreferrer noopener"
      class="project--link">Game of Life Visualizer</a
    >
  </div>
  <br />
  <div>
    <i class="lab la-github" />
    <a
      href="https://github.com/Jongtelles/game-of-life-viz"
      target="_blank"
      rel="noreferrer noopener"
      class="project--link">Github Repo</a
    >
  </div>
  <img
    class="project--img"
    alt="game of life vizualizer website screenshot"
    src="https://res.cloudinary.com/ushigoroshi/image/upload/f_auto,q_auto/v1617936399/gomeoflife_nwbvnl.png"
    loading="lazy"
  />
  <p class="project--desc" style="background-color: rgba(0, 0, 0, 25%);">
    React app that generates a board and randomly creates starting organisms before playing out
    iterations of the Game of Life
  </p>
</article>
<article class="project">
  <div>
    <i class="las la-link" />
    <a
      href="https://dogs-r-good-4-u.netlify.app/"
      target="_blank"
      rel="noreferrer noopener"
      class="project--link">Dogs R Good 4 U</a
    >
  </div>
  <br />
  <div>
    <i class="lab la-github" />
    <a
      href="https://github.com/Jongtelles/dogs-r-good-4-u"
      target="_blank"
      rel="noreferrer noopener"
      class="project--link">Github Repo</a
    >
  </div>
  <img
    class="project--img"
    alt="dogs r good 4 u website screenshot"
    src="https://res.cloudinary.com/ushigoroshi/image/upload/f_auto,q_auto/v1617936405/dogsrguud_g8eyxm.png"
    loading="lazy"
  />
  <p class="project--desc" style="background-color: rgba(0, 0, 0, 25%);">
    React app that utilizes Hooks to fetch dogs at random (continuously or one at a time) and makes
    them do tricks (CSS animations)'
  </p>
</article>

<style>
  div {
    display: grid;
    place-content: center;
    grid-auto-flow: column;
  }

  .project {
    flex-basis: 45%;
    background: linear-gradient(20deg, #64cff7, #8f8cf2, #ca7cd8, #ff68a8);
    box-shadow: -10px 10px 10px #18363e;
    transition: box-shadow 0.5s ease-in-out;
    padding: 1rem;
    margin: 2rem;
    border-radius: 1rem;
    border: 7px solid whitesmoke;
    max-width: 40rem;
  }

  .project:hover {
    box-shadow: 10px 15px 10px #18363e;
  }

  .project--link {
    color: whitesmoke;
    font-weight: bold;
    margin: 0 0.5rem;
  }

  .project--link:hover {
    color: #2e2157;
  }

  .project--img {
    display: block;
    margin: 1rem auto;
    border-radius: 1rem;
    max-width: 20rem;
    max-height: 24rem;
  }

  .project--desc {
    padding: 0.5rem;
    border-radius: 1rem;
    /* background-color: rgba(0, 0, 0, 25%); */
    font-size: 1.4rem;
  }

  @media (max-width: 500px) {
    .project {
      flex-basis: 100%;
    }
  }
</style>
