<style>
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
</style>

<body class="bg-zinc-700">
    <div class="flex justify-center w-screen-10 bg-red-300 m-2 rounded-md">

        <div class="m-3">
            <a href="/" class="underline">
                <p class="hover:scale-150 duration-150 text-zinc-700">Home</p>
            </a>
        </div>

        <div class="m-3 ">
            <a href="/aww" class="underline ">
                <p class="hover:scale-150 duration-150 text-zinc-700">Aww</p>
            </a>
        </div>

        <div class="m-3">
            <a href="fav" class="underline">
                <p class="hover:scale-150 duration-150 text-zinc-700" >Favourites</p>
            </a>
        </div>

    </div>
</body>
<slot></slot>