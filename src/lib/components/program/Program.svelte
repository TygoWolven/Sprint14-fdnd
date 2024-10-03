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
        max-width: 42rem;
        background-color: var(--lavender);
        color: var(--attention);
        border: 1px solid var(--lavender);
        margin-inline: .05em auto;
        margin-top: 0.25rem;
		margin-bottom: 1.25rem;
        padding: 1rem;
    }

    :global(section h2::selection, section p::selection) {
        background-color: var(--lavender);
        color: var(--lavender);
    }

    section::after {
        content: '';
        position: absolute;
        z-index: -1;
        top: var(--shadow);
        left: calc(var(--shadow) * -1.75);
        right: var(--shadow);
        bottom: calc(var(--shadow) * -1.75);
        border: 1px solid var(--lavender);
        border-radius: var(--rounded);
    }

    :global(section p) {
        font-size: 1rem;
        margin-top: 0.6em;
    }
</style>