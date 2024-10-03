<script>
	// Aggregate *.fdnd.nl names from github.com/fdnd
	import logo from '$lib/assets/Creating-logo.png' 
</script>

<footer>
	<nav>
		<h2>Archief</h2>
		<p>
			Hier kun je het programma van voorgaande studiejaren bekijken. 
		</p>
		<ul>
			<!-- <li><a href="https://2122.programma.fdnd.nl">Programma 2122</a></li> -->
			<li><a href="https://2223.programma.fdnd.nl">Programma 2022-2023</a></li>
			<li><a href="https://2324.programma.fdnd.nl">Programma 2023-2024</a></li>
		</ul>
	</nav>

	<nav>
		<h2>FDND Microsites</h2>
		<p>
			FDND maakt gebruik van microsites. 
			Microsites zijn kleine websites ter ondersteuning van een campagne, informatie over een product, dienst of voor een ander specifiek doel.
		</p>
		<ul>
			<li><a href="https://fdnd.nl">FDND.nl</a></li>
			<li><a href="https://contact.fdnd.nl">Contact en routebeschrijving</a></li>
			<li><a href="https://programma.fdnd.nl">Programma</a></li>
			<li><a href="https://partners.fdnd.nl">Partners</a></li>
			<li><a href="https://niveaumatrix.fdnd.nl">Niveaumatrix</a></li>
			<li><a href="https://docs.fdnd.nl">Documenten</a></li>
		</ul>
	</nav>
</footer>

<img alt="Hogeschool van Amsterdam" src={logo} />

<style>
	footer {
		display: flex;
		justify-content: center;
		font-size: 1rem;
		padding: 2rem 0;
	}

	img {
		height: 80px;
		margin-left: 2.2em;
	}

	h2 {
		margin: 0;
	}

	p {
		margin: 0 0 1em 0;
		max-width: 58ch;
	}

	ul {
		padding: 0;
		margin: 0;
		display: flex;
		flex-wrap: wrap;
		max-width: 30em;
	}

	ul li {
		padding: 0.7em 0.2em;
	}

	ul li a {
		position: relative;
		color: var(--blueberry);
		font-weight: 900;
		padding: 0.4em 0.6em;
		border: 1px solid var(--blueberry);
		border-radius: var(--rounded);
		text-decoration: none;
		background: var(--grey);
	}

	ul li a:hover {
		text-decoration: underline;
	}

	ul li a::before {
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
</style>
