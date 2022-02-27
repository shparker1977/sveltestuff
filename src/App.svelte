<script>
	import css from '$lib/css/app.css';
	import GenericComponent from "./GenericComponent.svelte";
	let myInput = "";
</script>

<main>
	<h1>Something Awesome is coming....</h1>
</main>

<section class="gatherInformation">
	<GenericComponent bind:someVar={myInput} />
</section>

<section class="displayInformaiton">
	Great input: {myInput}
</section>