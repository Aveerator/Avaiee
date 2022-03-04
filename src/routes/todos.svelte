<script lang="ts">
	import { titleBar } from '../stores/store';
	$titleBar = 'Todo List';
	let todos = [];

	function apply() {
		let namea = (<HTMLInputElement>document.getElementById('textinput')).value;
		if (namea == '') return;
		let importance = (<HTMLInputElement>document.getElementById('importance')).value;
		let arrlenght = todos.length;
		todos.push({ name: namea, done: false, importance: importance });
		todos = todos;
	}
</script>

<div class="maincontainer-flex columns-1">
	<input class="textinput" type="text" id="textinput" placeholder="Name of TODO"/> 
    <input class="textinput" type="text" id="importance" placeholder="Importance of TODO"/>
	<button on:click={apply} class="dogbutton">apply</button>
	{#each todos as todo}
		{#if todo.done}
			<p class="line-through">{todo.name} <input type="checkbox" bind:checked={todo.done} /></p>
		{:else}
			<p>{todo.name} <input type="checkbox" bind:checked={todo.done} /></p>
		{/if}
	{/each}
</div>
