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

{#if !submit}
    <Rating on:submit={submitHandler}/>
{:else}
    <Summary rating={rating}/>
{/if}



<!-- svelte-ignore a11y-click-events-have-key-events -->
<footer on:click={()=>submit=false}>
Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. 
Coded by <a href="#sutaC">sutaC</a>.
</footer>

<!-- --- -->
<style>




    footer {
        position: fixed;
        width: 100%;
        text-align: center;
        bottom: 0;
        tab-size: 10px;
    }

</style>