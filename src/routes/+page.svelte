<script>
    import Rating from "./Modul-Rating.svelte"
    import Summary from "./Modul-Summary.svelte"

    let submit = false;
    let rating;

    function submitHandler(e){
        const formData = new FormData(e.target);
        const data = {};
        for (let field of formData) {
            const [key, value] = field;
            data[key] = value;
        }
        rating = data.rate;
        submit = true;
    }

</script>
<!-- --- -->

<main>
    {#if !submit}
        <Rating on:submit={submitHandler}/>
    {:else}
        <Summary rating={rating}/>
    {/if}
</main>



<!-- svelte-ignore a11y-click-events-have-key-events -->
<footer on:click={()=>submit=false}>
Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. 
Coded by <a href="#sutaC">sutaC</a>.
</footer>

<!-- --- -->
<style>
    @import url('https://fonts.googleapis.com/css2?family=Overpass:wght@400;700&display=swap');

    * {
        font-family: Overpass, "Helvetica", sans-serif;   
    }

    :global(body) {
        margin: 0;
        padding: 0;
    }

    main {
        width: 100vw;
        height: 100vh;
        
        display: flex;
        justify-content: center;
        align-items: center;

        background-color:  hsl(216, 12%, 8%);
    }


    footer {
        position: fixed;
        width: 100%;
        text-align: center;
        bottom: 0;
        tab-size: 10px;
        font-size: 10px;
        color: white;
    }

</style>