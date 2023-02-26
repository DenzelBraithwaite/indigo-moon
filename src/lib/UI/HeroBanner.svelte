<script>
    import BtnBanner from './buttons/BannerButton.svelte';
</script>

<!-- DESKTOP -->
<div class="desktop">
    <div class="banner">
        <div class="content">
            <h1 class="title">Experience Indigo Moon's Magical Shop and Tarot</h1>
            <p class="subtitle">A Spiritual Feeling</p>
        </div>
        <!-- <BtnBanner color='purple' text='Get Started'/> -->
    </div>
</div>

<!-- Mobile -->
<div class="mobile">
    <h1 class="m__title"><span class="m__indigo">Indigo</span> Moon Tarot</h1>
    <h2 class="m__subtitle">A Spiritual Feeling</h2>
</div>

<style>
    .mobile {
        display: none;
    }

    .banner {
        position: relative;
        background-image: linear-gradient(to bottom, #ffffff17, #00000093),url(/bg.webp);
        width: 100vw;
        height: 70vh;
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center;

        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-evenly;
    }

    .content {
        font-family: cursive;
        color: #fff;
        width: 400px;
        height: 400px;
        margin: 0 auto;
        text-align: center;
        background-color: #fffafe86;
        box-shadow: 0 2px 20px #47a8f76c;
        border-radius: 50%;
    }

    .title {
        font-size: 3rem;
        line-height: 1.25;
        font-weight: 400;
        text-shadow: 0 2px 10px #000000c4;
    }

    .subtitle {
        font-size: 1.25rem;
        font-weight: lighter;
        text-shadow: 0 2px 10px #000000c4;
        margin-bottom: 1rem;
    }

    /* Mobile */
    @media (max-width: 1000px) {
        .desktop {
            display: none;
        }

        .mobile {
            z-index: 1;
            display: block;
            position: relative;
            color: #fff;
            background-color: #000000e1;
            margin: 0;
            padding: 0.5rem 0;
            text-align:center;
        }

        .m__indigo {
            color: #a782a5;
        }
    
        .m__title {
            margin: 0;
            padding: 0;
            font-size: 2rem;
        }
    
        .m__subtitle {
            margin: 0;
            padding: 0;
            font-weight: normal;
            font-size: 1rem;
        }
    }

</style>