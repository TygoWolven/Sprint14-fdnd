<script>
	import { page } from '$app/stores';

  	let navItems = [
    {
      href: '/static-web/the-client',
      title: 'Sprint 2'
    },
	{
		href: '/',
		title: 'FDND'
	},
    {
      href: '/workflow-tooling-frameworks/lose-your-head',
      title: 'Sprint 14'
    },
  ];

  const [firstItem, secondItem, thirdItem] = navItems;
</script>

<header>
  <div>
    <nav>
      <ul>
        <li>
          <a class:active={$page.url.pathname === firstItem.href} href={firstItem.href} target="_self">{firstItem.title}</a>
        </li>
        <li>
			<h1>
          <a class:active={$page.url.pathname === secondItem.href} href={secondItem.href} target="_self">
				{secondItem.title}
          </a>
		</h1>
        </li>
        <li>
          <a class:active={$page.url.pathname === thirdItem.href} href={thirdItem.href} target="_self">{thirdItem.title}</a>
        </li>
      </ul>
    </nav>
  </div>
</header>


<style>
	a {
		text-decoration: none;
		margin-left: var(--shadow);
	}

	h1{
		position: relative;
		color: var(--blueberry);
		font-size: 1.2rem;
		font-weight: 600;
		letter-spacing: -0.06em;
		padding: 0 0.6em;
		margin: 0;
		border-radius: var(--rounded);
	}

	@media (max-width: 750px) {
		h1 { color: var(--turquoise); }
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
		justify-content: center;
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

	ul {
		display: flex;
		justify-content: center	;
		gap: 1em;
		font-weight: 600;
	}

	nav ul li a {
		position: relative;
		transform: none;
		display: inline-block;
		padding: 0.3em 0.6em;
		border-radius: 1em;
		text-decoration: none;
		transition: background 0.3s ease-out, color 0.3s ease-out;
		white-space: nowrap;
	}

	nav ul li a:hover {border-color: var(--blueberry);}

	nav ul li a:hover::before { opacity: 1; }

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