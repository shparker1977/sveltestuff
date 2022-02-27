<script>
    export let someVar;
    let reverseVar = "";

    function mirrorInput() {
        reverseVar = someVar.split("").reverse().join("");
    }
</script>



<input type="text" class="genericInput" bind:value={someVar} on:input={mirrorInput}>
<p>Mirror of input</p>
<div class="mirrorDiv" contenteditable=true bind:innerHTML={reverseVar} />