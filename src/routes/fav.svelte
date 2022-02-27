<script>
	import { saved } from '../stores/store';
	function removeFromList(index) {
		$saved.splice(index, 1);
		$saved = $saved;
	}
</script>

<div class="topbar"><p class="m-3">Favourite Dog List</p></div>
<div class="maincontainer">
	<p class="text-main">
		Favourite dogs will appear here, add some in 'Aww' tab. Click the dog to remove
	</p>
	{#each $saved as dog, index}
		<img on:click={() => removeFromList(index)} src={dog} class="dogimg" alt={dog} />
	{/each}
</div>
