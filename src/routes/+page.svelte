<script>
    import Program from '$lib/components/program/Program.svelte';

    export let data

    const {title, subtitle, content, semesters} = data

</script>

<Program {title} {content} />
