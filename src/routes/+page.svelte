<script>
    import Program from '$lib/components/program/Program.svelte';
    import Semesters from '$lib/components/program/Semesters.svelte';
    import Topics from '$lib/components/program/sprint/Topics.svelte';

    export let data

    const {title, subtitle, content, semesters, topics, startdate} = data

</script>

<Program {title} {content} />
<Semesters {subtitle} {semesters} />
<Topics {topics} {startdate} />
