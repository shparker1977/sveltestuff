<script lang="ts">

export let nanogramPuzzleObject;
let numberOfColumns = nanogramPuzzleObject.Cells[0].length + 1;
console.log(numberOfColumns);

function handleCellClick() {

}

function checkIfPuzzleSolved() {
    
}

</script>

<div class="nanoPuzzle">
  <div class="noHeader"></div>
  {#each Array(nanogramPuzzleObject.Cells[0].length) as ColumnKey}
  <div class="keyCell"></div>
  {/each}
  {#each nanogramPuzzleObject.Cells as row, rowIndex}
    <div class="keyCell"></div>
    {#each row as cell, columnIndex}
    <div class="cell row{rowIndex} column{columnIndex}" 
         bind:this={cell} on:click={handleCellClick} >
    </div>
    {/each}
  {/each}
</div>

<style>
  .nanoPuzzle {
    padding: 10px;
    background-color: cornflowerblue;
    display: grid;
    width: fit-content;
    grid-template-columns: repeat(var(--numberOfColumns, 5), auto);

  }
  .cell {
    background-color: seashell;
    margin: 1px;
    min-width: 20px;
    max-width: 60px;
    min-height: 20px;
    max-height: 60px;
  }
  .keyCell {
    background-color: darkgrey;
    margin: 1px;
    min-width: 20px;
    max-width: 60px;
    min-height: 20px;
    max-height: 60px;
  }

</style>
