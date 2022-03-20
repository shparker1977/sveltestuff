<script>
	import Nanogram from './Nanogram.svelte'
	import nanogramJSONObject from './shared/files/nanogram/level1.json';
</script>

<main>
	<h1>Something Awesome is coming....</h1>
</main>

<section>
	A nanogram game written in svelte
	<br>
	<Nanogram nanogramPuzzleObject={nanogramJSONObject} />

</section>