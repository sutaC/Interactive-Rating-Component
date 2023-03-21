<script>
    export let rating = '1';
</script>
<!-- ---  -->

<div class="card">
    <img src="/illustration-thank-you.svg" alt="illustration-thank-you">
    <p class="selected">You selected {rating} out of 5</p>
    <h1>Thank you!</h1>
    <p>We appreciate you taking the time to give a rating. If you ever need more support, don’t hesitate to get in touch!</p>
</div>

<!-- ---  -->
<style>

    * {
        color: white;
        margin: 0;
        padding: 0;
    }

    p {
        color: hsl(217, 12%, 63%);
        font-size: 15px;
    }

    .card {
        width: 21rem;
        height: 19rem;

        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        gap: 1rem;

        padding: 2rem 1rem;

        border-radius: 2rem;

        background: radial-gradient(ellipse at top, hsl(213, 19%, 18%), hsla(213, 20%, 18%, 0.4));
    }

    .selected {
        display: flex;
        justify-content: center;
        align-items: center;

        width: 55%;
        height: 1.8rem;
        border-radius: 1rem;

        color: hsl(25, 97%, 53%);
        background-color:  hsla(216, 12%, 54%, 0.2);
    }

</style>