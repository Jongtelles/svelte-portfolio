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

<style lang="scss">
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
</style>
