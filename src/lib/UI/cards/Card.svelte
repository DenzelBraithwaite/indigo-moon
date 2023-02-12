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
        background-color: #fff;
    }

    .card img {
        width: 100%;
        height: 40%;
        padding-bottom: 1rem;
        object-fit: cover;
    }

    .text-section {
        position: relative;
        display: flex;
        flex-direction: column;
        width: 80%;
        height: 50%;
        margin: 0 auto;
        padding-bottom: 1rem;
        justify-content: space-between;
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
    <div class="text-section">
        <div class="content">
            <h1 class="title">{title}</h1>
            <p class="duration">{duration}</p>
            <p class="cost">{cost}</p>    
        </div>
        <Button text="Book Now"/>
    </div>
</div>