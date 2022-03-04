<script>
	/*All TailwindCSS in this file*/
	import '../style.postcss';

	import { titleBar } from "../stores/store"
</script>

<!-- main top bar with divs for every entry -->
<body class="bg-main">
	<div class="topbar">
		<div class="m-3">
			<a href="/">
				<p class="entry">Home</p>
			</a>
		</div>
		<div class="m-3">
			<a href="/aww">
				<p class="entry">Aww</p>
			</a>
		</div>
		<div class="m-3">
			<a href="fav">
				<p class="entry">Favourites</p>
			</a>
		</div>
		<div class="m-3">
			<a href="todos">
				<p class="entry">Todos</p>
			</a>
		</div>
	</div>
</body>

<div class="topbar"><p class="m-3">{$titleBar}</p></div>

<slot />

<div class="topbar fixed bottom-0 "><p class="m-3">AVIEE // <a href="https://github.com/Aveerator/Avaiee" class="underline">source code</a></p></div>
