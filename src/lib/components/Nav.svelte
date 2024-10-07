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

	nav ul li a {
		position: relative;
		font-size: 1.15rem;
		transform: none;
		display: inline-block;
		padding: 0.25em 0.5em;
		text-decoration: none;
		white-space: nowrap;
		text-decoration: none;
		margin-left: var(--shadow);
		color: var(--attention);
		background-color: var(--lavender);
		border-radius: 12px;
		border: 1px solid var(--attention);
		outline: none;
		transition: all 0.3s ease-out; 
	}

	nav ul li a::before{
		content: '';
		position: absolute;
		width: 100%;
		height: 100%;
		z-index: -1;
		border: 1px solid var(--attention);
		border-radius: 12px;
		top: calc(var(--shadow) * .85);
		left: calc(var(--shadow) * -.85);
		right: calc(var(--shadow) * -.75);
		transition: all 0.3s ease-out;
	}

	header nav ul li h1 {
		position: relative;
		color: var(--white);
		font-size: 1.2rem;
		font-weight: 600;
		letter-spacing: -0.06em;
		padding: 0 0.75em;
		margin: 0;
		border-radius: var(--rounded);
	}

	nav ul li a.active {
		background-color: var(--attention);
		color: var(--white);
		padding: .25em .75em;
		transform: translateY(1px);
	}

	nav ul li a:active, nav ul li a:focus {
		background-color: var(--attention);
		color: var(--white);	
		transform: translateY(1px);
	} 
</style>
