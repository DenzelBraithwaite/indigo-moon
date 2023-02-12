<script>
    // JavaScript Below
    import Button from '../buttons/Button.svelte'

    export let src;
    export let alt;
    export let title = '';
    export let duration = '';
    export let cost = '';
</script>

<style>
    /* CSS Below */
    .card {
        position: relative;
        border: 1px solid #727557a1;
        width: 300px;
        background-color: #fff;
    }

    .card img {
        width: 100%;
        padding-bottom: 1rem;
    }

    .text {
        width: 80%;
        margin: 0 auto;
        padding-bottom: 1rem;
    }

    .title {
        font-weight: 500;
        font-size: 1.5rem;
        padding-bottom: 1rem;
        border-bottom: 1px solid #72755767;
    }
</style>

<!-- HTML Below -->
<div class="card">
    <img {src} {alt}>
    <div class="text">
        <h1 class="title">{title}</h1>
        <p class="duration">{duration}</p>
        <p class="cost">{cost}</p>
        <Button text="Book Now"/>
    </div>
</div>