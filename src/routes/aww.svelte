<script lang="ts">
	import { saved, titleBar } from '../stores/store';
	let data = { message: 'no' };
	function getDog() {
		fetch('https://dog.ceo/api/breeds/image/random')
			.then((response) => response.json())
			.then((dog) => (data = dog));
	}
	function saveDog() {
		if (!$saved.includes(data.message) || data.message != 'no') $saved.push(data.message);
	}
	$titleBar = "Random Dog Generator"
</script>

<div class="maincontainer">
	<p class="self-center text-main">
		Wanna see a cute picture of a dog? Click on the dog to save it to favourites seen in
		'Favourites' tab
	</p>
	<button class="dogbutton" on:click={getDog}>Yes</button>
	<img on:click={saveDog} src={data.message} class="dogimg" alt="*dog goes here*" />
</div>
