<script>
	import logo from '$lib/images/TASLA logo.png';
</script>

<header>
	<div class="corner">
		<img src={logo} alt="TASLA"/>
	</div>

	<nav class="corner">
		<ul>
			<li>
				<a href="/" class="title">Home</a>
			</li>
			<li>
				<a href="/" class="title">Our Organization</a>
			</li>
			<li>
				<a href="/" class="title">Scholars</a>
			</li>
			<li>
				<a href="/" class="title">Sponsors</a>
			</li>
		</ul>
	</nav>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.title {
		color: #F5F5F5;
		font-weight: 600;
		font-size: 1em;
	}

	.corner {
		align-items: center;
		width: auto;
		height: 4em;
		color: black;
	}

	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	.corner img {
		padding-left: 2em;
		width: 8em;
		height: 6em;
		object-fit: contain;
	}

	/* svg {
		width: 2em;
		height: 3em;
		display: block;
	}

	path {
		fill: var(--background);
	} */

	ul {
		height: 5em;
		padding-right: 2em;
		display: flex;
		align-items: center;
		list-style: none;
	}

	li {
		position: relative;
		height: 100%;
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-theme-1);
	}
</style>