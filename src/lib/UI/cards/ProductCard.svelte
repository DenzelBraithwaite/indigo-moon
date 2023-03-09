<script>
    import Button from '../buttons/Button.svelte'

    export let src;
    export let alt;
    export let title = '';
    export let description = '';
    export let cost = '';
    export let btnText = '';
    export let path;
    export let hover;
</script>

<a class="product-card" href={path}>
    <img {src} {alt}>
    <div class="text-section">
        <div class="content">
            <h1 class="title">{title}</h1>
            <p class="description">{description}</p>
            <p class="cost">{cost}</p>    
        </div>
        <Button {hover} {path} color='purple' text={btnText}/>
    </div>
</a>

<style>
    .product-card:link,
    .product-card:visited {
        color: var(--primary-grey);
        text-decoration: none;
        position: relative;
        background-color: #ffffff;
        box-shadow: 2px 0 10px #00000034;
        border-radius: 0.5rem;
        transition: scale 0.1s ease-in;
    }

    .product-card:hover,
    .product-card:active {
        color: var(--primary-grey);
        cursor: pointer;
        scale: 1.1;
        box-shadow: 0 2px 20px #47a8f721;
        transition: scale 0.25s ease-out;
    }

    .product-card img {
        width: 275px;
        height: 250px;
        object-fit: cover;
        border-radius: 0.5rem 0.5rem 0 0;
        
    }

    .content {
        height: 150px;
    }

    .text-section {
        display: flex;
        flex-direction: column;
        width: 80%;
        margin: 0 auto;
        padding-bottom: 1rem;
        justify-content: space-between;
    }

    .title {
        font-weight: 500;
        font-size: 1.2rem;
        padding-bottom: 1rem;
        border-bottom: 1px solid #65466483; /* var(--secondary-purple), transparent*/
    }

    .cost {
        font-size: 0.85rem;
        margin: 0;
        height: 1.5rem;
        width: 4rem;
        color: #fff;
        background-color: #47a8f7e5;
        border-radius: 50px;

        display: flex;
        justify-content: center;
        align-items: center;

        position: absolute;
        top: 1rem;
        left: -2rem;
    }

    @media (max-width: 1000px) {
        .product-card:hover,
        .product-card:active {
            scale: 1;
        }

        .product-card img {
            width: 250px;
        }

        .text-section {
            display: flex;
            flex-direction: column;
            width: 90%;
            padding-bottom: 0;
        }
    }
</style>