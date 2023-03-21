<script>

    let selected = 0;

</script>
<!-- ---  -->

<form on:submit|preventDefault>
    <div class="circle">
        <img src="/icon-star.svg" alt="icon-star">
    </div>
    <h1>How did we do?</h1>
    <p>Please let us know how we did with your support request. All feedback is appreciated to help us improve our offering!</p>

    <input type="radio" name="rate" id="rate1" value="1" required>
    <input type="radio" name="rate" id="rate2" value="2" required>
    <input type="radio" name="rate" id="rate3" value="3" required>
    <input type="radio" name="rate" id="rate4" value="4" required> 
    <input type="radio" name="rate" id="rate5" value="5" required>

    <div class="rating" >
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <label for="rate1" class="circle" class:selected={selected === 1} on:click={()=>selected=1}>1</label>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <label for="rate2" class="circle" class:selected={selected === 2} on:click={()=>selected=2}>2</label>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <label for="rate3" class="circle" class:selected={selected === 3} on:click={()=>selected=3}>3</label>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <label for="rate4" class="circle" class:selected={selected === 4} on:click={()=>selected=4}>4</label>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <label for="rate5" class="circle" class:selected={selected === 5} on:click={()=>selected=5}>5</label>
    </div>

    <button type="submit">Submit</button>
</form>

<!-- ---  -->
<style>

    * {
        color: white;
        margin: 0;
        padding: 0;
    }

    p, label{
        color: hsl(217, 12%, 63%);
        font-size: 15px;
    }

    form {
        width: 21rem;
        height: 19rem;

        display: flex;
        flex-direction: column;
        justify-content: center;
        gap: 1rem;

        padding: 2rem 1rem;

        border-radius: 2rem;

        background: radial-gradient(ellipse at top, hsl(213, 19%, 18%), hsla(213, 20%, 18%, 0.4));
    }


    input {
        display: none;
    }

    button {

        width: 90%;
        height: 2.5rem;
        
        align-self: center;

        border: none;
        border-radius: 2rem;
        outline: none;

        background-color:  hsl(25, 97%, 53%);

        text-transform: uppercase;
    }

    button:active {
        background-color: #fff;
        color: hsl(25, 97%, 53%);
    }


    .circle {
        width: 2.8rem;
        height: 2.8rem;

        border-radius: 100%;

        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;

        background-color:  hsla(216, 12%, 54%, 0.2);
    }


    .rating {
        display: flex;
        justify-content: space-around;
        align-items: center;
        flex: 1;
    }

    .rating label {
        cursor: pointer;
    }

    .rating label:not(.selected):hover {
        background-color: hsl(216, 12%, 54%);
        color: white;
    }

    .selected {
        background-color: hsl(25, 97%, 53%);
        color: white;
    }

</style>