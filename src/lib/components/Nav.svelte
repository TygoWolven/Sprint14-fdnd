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

	import logo from '$lib/assets/HvA-logo.png';
</script>

<header>
	<div>
		<img alt="The project logo" src={logo} />
		<p>Frontend Design & Development</p>
	</div>
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
		padding: 0 1.5em;
	}

	h1 { 
		margin: 0; 
	}

	h1 > abbr {
		position: relative;
		color: var(--blueberry);
		font-size: 1.4rem;
		font-weight: 900;
		letter-spacing: -0.1em;
		padding: 0.2em 0.4em;
		border: 1px solid var(--blueberry);
		border-radius: var(--rounded);
		text-decoration: none;
		background: var(--grey);
		left: 15px;
		bottom: 3.1em;
	}

	h1 > abbr::before {
		content: '';
		width: 100%;
		height: 100%;
		position: absolute;
		border: 1px solid var(--blueberry);
		border-radius: var(--rounded);
		background: var(--grey);
		z-index: -10;
		top: 2px;
		right: 2px;
	}

	header div {
		display:flex;
		max-width: var(--max-width);
		flex-wrap:nowrap;
		align-items: baseline;
		justify-content: space-between;
		margin-left: 2em;
	}

	header div:first-of-type {
		justify-content: start;
		align-items: center;
		padding-bottom: 1em;
	}

	header img {
		height: 90px;
		margin-top: 0.2em;
		margin-right: -1.7em;
	}

	header p {
		color: var(--blueberry);
		border-left: 1px solid var(--blueberry);
		padding: 0 1em;
		font-size: 1.2em;
		letter-spacing: -0.03em;
	}

	nav {
		position: relative;
		font-size: 0.8rem;
		background-color: var(--grey);
		color: var(--blueberry);
		border-radius: 15px 15px 0 0;
		margin-top: 3em;
	}

	nav::before {
		content: '';
		position: absolute;
		width: 1.5em;
		aspect-ratio: 1;
		left: -1.5em;
		border-radius: 0 0 50% 0;
		bottom: 0;
		box-shadow: 0.5em 0.5em 0 0 var(--grey);
	}

	h2 {
		position: absolute;
		text-indent: -9999px;
	}
	ul {
		display: flex;
		font-weight: 500;
		padding: 0 4em;
	}

	nav ul li a {
		position: relative;
		transform: none;
		display: inline-block;
		letter-spacing: -0.03em;
		border-radius: 1em;
		text-decoration: none;
		transition: background 0.3s ease-out, color 0.3s ease-out;
		white-space: nowrap;
		color: var(--blueberry);
		top: 3px;
	}

	nav ul li a:hover {
		text-decoration: underline;
	}

	@media (max-width: 750px) {
		nav ul {
			font-size: 0.75em;
		}

		:global(nav a.active) {
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