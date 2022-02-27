<script>
    /*All TailwindCSS in this file*/
    import "../style.postcss"
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

    </div>
</body>

<slot></slot>