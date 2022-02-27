<script context="module">
	export function load({ error, status }) {
		return {
			props: {
				title: `${status}: ${error.message}`,
				status: `${status}`
			}
		};
	}
</script>

<script>
	export let title;
	export let status;
	export let message = '';
	if (status == '404') {
		message = 'Navigate to other page using the top bar';
	} else {
		message = 'probably something broke ';
	}
</script>

<div class="topbar"><p class="m-3">This is error</p></div>
<div class="maincontainer">
	<p class="text-6xl text-main">ERROR</p>
	<p class="text-main">{title}</p>
	<p class="text-main">{message}</p>
</div>
