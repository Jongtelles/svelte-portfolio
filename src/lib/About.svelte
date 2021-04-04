<div class="about">
	<h2>About Me</h2>
	<div class="flex-container flex-evenly">
		<div class="about--img" alt="headshot of a very cool and handsome smiling man (it's me)" />
		<div class="about--list-container">
			<ul class="about--list">
				<li>
					<i class="fab fa-node-js" />
					Full Stack Web Developer that loves JavaScript
				</li>
				<li>
					<i class="far fa-comments" />
					Strong communicator with a knack for translating technical concepts into plain English (or
					terrible Spanish)
				</li>
				<li>
					<i class="fas fa-rocket" />
					Able to quickly implement new technologies; I live for solving complex problems and learning
					new things
				</li>
				<li>
					<i class="fas fa-brain" />I don't know how to do everything, but I know how to find out
					how to do <em>anything</em>
				</li>
				<li>
					<i class="fas fa-coffee" />I’ll <strong>always</strong> make the coffee
				</li>
			</ul>
		</div>
	</div>
	<p class="about--tech-skills">
		<strong>Stack 🥞:</strong> React (Hooks) | Vue | TypeScript | Node | JavaScript (ES2015+) | SCSS/SASS | CSS3
		(animations) | HTML5 | jQuery
		<br />
		<strong>Data 💾:</strong> JSON | GraphQL | MySQL | MongoDB | REST | APIs
		<br />
		<strong>Misc 🔀:</strong> Git | Testing (Cyprus) | Design Systems | Agile | JIRA | InVision
		| BEM | 508 compliance | NPM | Babel | Docker | Gulp
		<br />
		<strong>Looking Into 👀:</strong> Svelte | Deno | Dgraph | Kubernetes | FaunaDB | Gatsby | WASM |
		Rust
	</p>
</div>

<style>
	.about {
		position: relative;
		background: linear-gradient(#200d3a, #292651, #2e4770, #ce5e82, #eca089, #ecc6a2);
		box-shadow: -10px 10px 10px #2e4770;
		padding: 1rem;
		margin: 2rem auto;
		border-radius: 1rem;
		transition: box-shadow 0.5s ease-in-out;
		border: 10px solid whitesmoke;
		max-width: 100rem;
	}

	.about:hover {
		box-shadow: 25px 25px 10px #2f9395;
	}

	.about--img {
		margin: 0.5rem;
		border-radius: 1rem;
		background-image: url(./assets/headshot2.0.png);
		background-size: cover;
		background-repeat: no-repeat;
		height: 24rem;
		width: 20rem;
		transition: background-image 0.5s ease-in-out;
	}

	.about--img:hover {
		background-image: url(./assets/headshot-8bit.gif);
	}

	.about--list-container {
		flex-basis: 50%;
	}

	.about--list {
		text-align: left;
	}

	.about--list li {
		margin: 0.75rem 0;
	}

	.about--list li i {
		margin-right: 0.5rem;
	}

	.about--tech-skills {
		color: #2e2157;
	}
</style>
