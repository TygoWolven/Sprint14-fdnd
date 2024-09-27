<script>
	import { page } from '$app/stores';
	$: navItems = [
		{
			href: '/',
			title: 'Programma 2425'
		},
		{
			href: '/static-web/the-client',
			title: 'Sprint 2'
		},
		{
			href: '/workflow-tooling-frameworks/lose-your-head',
			title: 'Sprint 14'
		},
	]

</script>

<header>
	<div>
		<a href="/">
			<h1>
				<abbr title="Frontend Design &amp; Development"> <span>FDND</span> </abbr>
			</h1>
		</a>
		<nav>
			<h2>Menu</h2>
			<ul>
				{#each navItems as item }
					<li>
						<a class:active={$page.url.pathname === item.href} href={item.href} target="_self">{item.title}</a>
					</li>
				{/each}
			</ul>
		</nav>
	</div>
	
</header>


<style>
	a {
		text-decoration: none;
		margin-left: var(--shadow);
	}

	h1 { margin: 0; }

	h1 > abbr {
		position: relative;
		color: var(--blueberry);
		font-size: 1.2rem;
		font-weight: 600;
		letter-spacing: -0.06em;
		padding: 0.3em 0.2em;
		border: 1px solid var(--blueberry);
		border-radius: var(--rounded);
	}

	@media (max-width: 750px) {
		h1 > abbr { color: var(--turquoise); }

	}

	h1 > abbr::before {
		content: '';
		position: absolute;
		top: var(--shadow);
		left: calc(var(--shadow) * -1);
		right: var(--shadow);
		bottom: calc(var(--shadow) * -1);
		border: 1px solid currentColor;
		border-radius: var(--rounded);
		display:none;
	}

	header {
		display:flex;
		max-width: var(--max-width);
		margin: auto;
	}

	header div {
		display: flex;
		gap: 1em;
		align-items: baseline;
		justify-content: flex-start;
		padding: 0.5em 0.7em calc(0.5em + var(--shadow));
		background-color: var(--turquoise);
		color: var(--blueberry);
		border-radius: var(--rounded);
		flex-wrap:nowrap;
	}

	@media (max-width: 750px) {
		header div {
			background-color: transparent;
			padding: 0;
			gap: 1em;
		}
	}

	nav {
		font-size: 0.8rem;
		width: 80vw;
	}

	h2 {
		position: absolute;
		text-indent: -9999px;
	}
	ul {
		display: flex;
		gap: 1em;
		font-weight: 600;
	}

	nav ul li a {
		position: relative;
		transform: none;
		display: inline-block;
		padding: 0.3em 0.8em;
		border-radius: 1em;
		text-decoration: none;
		transition: background 0.3s ease-out, color 0.3s ease-out;
		border: 1px solid var(--turquoise);
		white-space: nowrap;
	}
	nav ul li a:hover {border-color: var(--blueberry);}

	nav ul li a:hover::before {
		opacity: 1;
	}

	:global(nav a.active) {
		font-weight: 800;
		background-color: var(--blueberry);
		color: var(--turquoise);
	}

	@media (max-width: 750px) {
		nav ul {
			font-size: 0.75em;
			color: var(--turquoise);
		}

		nav ul li a:hover {
			border-color: var(--turquoise);
		}

		:global(nav a.active) {
			background-color: var(--turquoise);
			color: var(--blueberry) !important;;
		}
	}

	@media (min-width: 22em) {
		nav { font-size: 1rem; }
	}

	@media (min-width: 42em) {
		nav { margin-bottom: 0; }
		nav ul a { transform: rotate(-5deg); }
	}
</style>