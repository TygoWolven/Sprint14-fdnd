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
    <nav>
      <ul>
        <li>
          <a class:active={$page.url.pathname === firstItem.href} href={firstItem.href} target="_self">{firstItem.title}</a>
        </li>
        <li>
			<h1>
        		<a class:active={$page.url.pathname === secondItem.href} href={secondItem.href} target="_self"> {secondItem.title} </a>
			</h1>
        </li>
        <li>
          <a class:active={$page.url.pathname === thirdItem.href} href={thirdItem.href} target="_self">{thirdItem.title}</a>
        </li>
      </ul>
    </nav>
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
		padding: 0 0.75em;
		margin: 0;
		border-radius: var(--rounded);
	}

	@media (max-width: 750px) {
		h1 { color: var(--turquoise); }
	}

	header {
		display: flex;
		align-items: baseline;
		justify-content: center;
		width: 60%;
		margin: -2.25em auto 2.75em auto;
		padding: 0.75em;
		background-color: var(--turquoise);
		color: var(--blueberry);
		border-radius: 0 0 120px 120px;
		flex-wrap: nowrap;
	}

	@media (max-width: 750px) {
		header {
			background-color: transparent;
			padding: 0;
			margin-top: -1em;
			gap: 1em;
		}
	}

	nav {
		font-size: 0.8rem;
	}

	ul {
		display: flex;
		justify-content: center	;
		gap: 1.5em;
		font-weight: 600;
	}

	nav ul li a {
		position: relative;
		font-size: 1.15rem;
		transform: none;
		display: inline-block;
		padding: 0.25em 0.5em;
		border-radius: 12px;
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