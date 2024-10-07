<script>
	import Program from '$lib/components/program/Program.svelte';
	import Semesters from '$lib/components/program/Semesters.svelte';

	export let data;

	const { title, subtitle, content, semesters } = data;
</script>

<Program {title} {content} />
<Semesters {subtitle} {semesters} />

<style>
	:global(body:before) {
		width: 160px;
	}
	:global(body:after) {
		width: 160px;
	}
	@media (min-width: 40em) {
		:global(body:before) {
			width: 350px !important;
		}
	}
</style>
