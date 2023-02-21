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
    .product-card {
        position: relative;
        background-color: #fff;
        /* max-width: 400px; causing horizontal align issues*/
        box-shadow: 2px 0 10px #00000034;
        border-radius: 8px;
    }

    .product-card img {
        width: 100%;
        height: 50%;
        padding-bottom: 1rem;
        object-fit: cover;
        border-radius: 8px 8px 0 0;
        
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
        border-bottom: 1px solid #4c368f64;
        height: 5rem;
    }


</style>

<!-- HTML Below -->
<div class="product-card">
    <img {src} {alt}>
    <div class="text-section">
        <div class="content">
            <h1 class="title">{title}</h1>
            <p class="duration">{duration}</p>
            <p class="cost">{cost}</p>    
        </div>
        <Button color='purple' text="Book Now"/>
    </div>
</div>