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
        position: relative;
        text-decoration: none;
        max-width: 250px;
        color: var(--primary-grey);
        background-color: #ffffff;
        box-shadow: 2px 0 8px #0000001f;
        border-radius: 0.5rem;
        transition: scale 0.1s ease-inww;
    }

    .product-card:hover,
    .product-card:active {
        color: var(--primary-grey);
        cursor: pointer;
        scale: 1.1;
        box-shadow: 2px 0 20px #00000011;
        transition: scale 0.25s ease-out;
    }

    .product-card img {
        width: 100%;
        height: 45%;
        object-fit: cover;
        border-radius: 0.5rem 0.5rem 0 0;
        
    }

    .description {
        margin-bottom: 0;
        font-size: 0.9rem;
        white-space: normal;
        overflow: hidden;
        text-overflow: ellipsis;
        display: -webkit-box;
        -webkit-box-orient: vertical;
        -webkit-line-clamp: 2;
    }

    .text-section {
        height: 50%;
        display: flex;
        flex-direction: column;
        width: 85%;
        margin: 0 auto;
        justify-content: space-between;
    }

    .title {
        text-align: center;
        font-size: 0.9rem;
        padding-bottom: 0.3rem;
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
        .product-card:link,
        .product-card:visited {
            position: relative;
            text-decoration: none;
            max-width: 200px;
            color: var(--primary-grey);
            background-color: #ffffff;
            box-shadow: 2px 0 8px #0000001f;
            border-radius: 0.5rem;
            transition: scale 0.1s ease-inww;
        }
    }

    @media (max-width: 450px) {
        .product-card:hover,
        .product-card:active {
            scale: 1;
        }
    }
</style>