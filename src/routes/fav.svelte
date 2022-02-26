<script>
    import { saved } from "../stores/store"
    function removeFromList(index) {
		$saved.splice(index, 1)
		$saved = $saved;
    }
</script>

<div class="flex justify-center w-screen-10 bg-red-300 m-2 rounded-md p-3 text-zinc-700">Favourite Dog List</div>
<div class="md:grid grid-cols-5 content-center gap-11h-full w-screen-10 bg-red-300 m-2 rounded-md p-14 sm:flex text-zinc-700" >
    Favourite dogs will appear here, add some in 'Aww' tab. Click the dog to remove
    {#each $saved as dog, index}
    <img on:click={() => removeFromList(index)} src={dog} class="lg:h-96 bg-cover self-center rounded-md text-zinc-700 hover:drop-shadow-2xl duration-75 m-4 p-4 object-scale-down" alt={dog}>
    {/each}
</div>