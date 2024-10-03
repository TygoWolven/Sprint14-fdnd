<script>
	import Heading from '$lib/components/Heading.svelte';

	export let title, content;
</script>

<section class="rounded col-span-2">
	<Heading {title} />
	{@html content.html}
</section>

<style>
 section {
        position: relative;
        max-width: 48rem;
        background-color: var(--blueberry);
        color: var(--turquoise);
        border: 1px solid var(--turquoise);
        margin-inline: .05em auto;
        margin-top: 0.25rem;
		margin-bottom: 1.25rem;
        padding: 1rem;
        grid-column: 1 / 2;
    }
    
    @media (max-width: 750px) {
        section { width: 100%; }
    }

    :global(section h2::selection, section p::selection) {
        background-color: var(--turquoise);
        color: var(--blueberry);
    }

    section::after {
        content: '';
        position: absolute;
        z-index: -1;
        top: var(--shadow);
        left: calc(var(--shadow) * -1);
        right: var(--shadow);
        bottom: calc(var(--shadow) * -1);
        border: 1px solid currentColor;
        border-radius: var(--rounded);
    }

    :global(section p) {
        font-size: 1rem;
        margin-top: 0.6em;
    }
</style>
