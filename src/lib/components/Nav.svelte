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
		}
	];

	const [firstItem, secondItem, thirdItem] = navItems;
</script>

<header />
<nav>
	<ul>
		<li>
			<a class:active={$page.url.pathname === firstItem.href} href={firstItem.href} target="_self" >{firstItem.title}</a>
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

<style>
	header {
		width: 100%;
		height: 2.5em;
		background-color: var(--lavender);
	}

	nav {
		position: sticky;
		display: flex;
		align-items: baseline;
		justify-content: center;
		width: 40%;
		height: 3.75em;
		margin: -.05em auto 3em auto;
		background-color: var(--lavender);
		color: var(--attention);
		border-radius: 0 0 120px 120px;
		flex-wrap: nowrap;
		font-size: 0.8rem;
	}

	@media (max-width:750px){
		nav{
			width: 90%;
		}
	}

	@media (min-width:750px) and (max-width:1024px){
		nav{
			width: 60%;
		}
	}

	nav ul {
		display: flex;
		justify-content: center;
		gap: 1.75em;
		padding-inline: 0;
		font-weight: 600;
		list-style-type: none;
		align-items: baseline;
		margin-top: -1em;
	}

	h1{
		font-size: 0.8rem;
	}

	a {
        position: relative;
        z-index: 1;
        border: 1px solid var(--attention);
        padding: .75rem;
        background-color: var(--white);
        border-radius: 10px;
        color: var(--attention);
        font-weight: 700;
        text-decoration: none;
    }

	a:focus-visible, a:hover {
		background-color: var(--call-to-action);
		right: 1px;
        top: 1px;
		transition: all .4s ease-out;
	}

	a:focus-visible::after, a:hover::after {
		background-color: #b1b073;
		right: 1px;
        top: 1px;
	}

	a.active{
		background-color: var(--turquoise);
		color: var(--attention);
	}

	a.active::after {
		background-color: #5c9c89;
	}

    a::after {
        content: "";
        z-index: -1;
        position: absolute;
        width: 100%;
        height: 100%;
        border: 1px solid var(--attention);
        background-color: var(--white);
        border-radius: 10px;
        color: var(--attent);
        right: 2px;
        top: 2px;
    }
</style>
