<script>
    import { saved } from "../stores/store"
    function removeFromList(index) {
		$saved.splice(index, 1)
		$saved = $saved;
    }
</script>

<div class="flex justify-center w-screen-10 bg-red-300 m-2 rounded-md p-2">Favourite Dog List</div>
<div class="md:grid grid-cols-3 content-center gap-11h-full w-screen-10 bg-red-300 m-2 rounded-md p-12 sm:flex" >
    Favourites appear here, click to remove
    {#each $saved as dog, index}
    <img on:click={() => removeFromList(index)} src={dog} class="lg:h-96 bg-cover self-center rounded-md" alt={dog}>
    {/each}
</div>