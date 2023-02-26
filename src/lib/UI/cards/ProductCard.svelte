<script>
    // JavaScript Below
    import Button from '../buttons/Button.svelte'

    export let src;
    export let alt;
    export let title = '';
    export let description = '';
    export let cost = '';
    export let btnText = '';
</script>

<!-- HTML Below -->
<div class="product-card">
    <img {src} {alt}>
    <div class="text-section">
        <div class="content">
            <h1 class="title">{title}</h1>
            <p class="description">{description}</p>
            <p class="cost">{cost}</p>    
        </div>
        <Button color='purple' text={btnText}/>
    </div>
</div>

<style>
    /* CSS Below */
    .product-card {
        position: relative;
        background-color: #fff;
        box-shadow: 2px 0 10px #00000034;
        border-radius: 0.5rem;
    }

    .product-card img {
        width: 300px;
        height: 250px;
        object-fit: cover;
        border-radius: 0.5rem 0.5rem 0 0;
        
    }

    .text-section {
        position: relative;
        display: flex;
        flex-direction: column;
        width: 80%;
        margin: 0 auto;
        padding-bottom: 1rem;
        justify-content: space-between;
    }

    .title {
        font-weight: 500;
        font-size: 1.25rem;
        padding-bottom: 1rem;
        border-bottom: 1px solid #65466483; /* var(--secondary-purple), transparent*/
    }
</style>