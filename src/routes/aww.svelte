
<script lang="ts">
    import { saved } from "../stores/store"
    let text = {message: "no"};
    function getDog() {
      fetch("https://dog.ceo/api/breeds/image/random")
        .then(response => response.json())
        .then(dog => text = dog)
    }
    function saveDog() {
        if (!($saved.includes(text.message) || text.message == "no")) {
            $saved.push(text.message);
        }         
    }
</script>
<div class="flex justify-center w-screen-10 bg-red-300 m-2 rounded-md p-2">Random Dog Generator</div>

<div class="md:grid grid-cols-3 content-center gap-11h-full w-screen-10 bg-red-300 m-2 rounded-md p-12 sm:flex" >

    <p class="self-center">Wanna see a cute picture of a dog? Click on the picture to save it to favourites</p>

    <button class="bg-zinc-700 p-10 rounded-md m-10" on:click={getDog}>Yes</button>

    <img on:click={saveDog} src={text.message} class="lg:h-96 bg-cover self-center rounded-md" alt="*dog goes here*">
    
</div>