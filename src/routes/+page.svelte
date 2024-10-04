<script>
    import Program from '$lib/components/program/Program.svelte';
    import Semesters from '$lib/components/program/Semesters.svelte';

    export let data

    const {title, subtitle, content, semesters} = data

</script>

<Program {title} {content} />
<Semesters {subtitle} {semesters} />
