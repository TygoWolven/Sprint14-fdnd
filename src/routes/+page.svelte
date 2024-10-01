<script>
    import Semesters from '$lib/components/program/Semesters.svelte'

    export let data
   
    const {title, subtitle, content, semesters} = data
</script>

<Semesters {semesters} {subtitle} />

<h1>Welcome to SvelteKit</h1>

<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
