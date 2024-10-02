<script>
    import Semesters from '$lib/components/program/Semesters.svelte'

    export let data
   
    const {title, subtitle, content, semesters} = data
</script>

<Semesters {semesters} {subtitle} />