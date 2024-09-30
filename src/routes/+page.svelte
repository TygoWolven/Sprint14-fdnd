<script>
    import Program from '$lib/components/program/Program.svelte';

    export let data

    const {title, subtitle, content, semesters} = data

</script>

<Program {title} {content} />

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
