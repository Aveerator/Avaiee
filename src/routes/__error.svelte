<script context="module">
	export function load({ error, status }) {
		return {
			props: {
				title: `${status}: ${error.message}`
			}
		};
	}
</script>

<script>
	import {titleBar} from "../stores/store"
	$titleBar = "I am error"
	export let title;
	export let message = errorMessage();
	function errorMessage() {
		if (title.startsWith('404')) return('Navigate to other page using the top bar')
		return('Probably something broke lolz')
	}
</script>
<div class="maincontainer">
	<p class="text-6xl text-main">ERROR</p>
	<p class="text-main">{title}</p>
	<p class="text-main">{message}</p>
</div>
