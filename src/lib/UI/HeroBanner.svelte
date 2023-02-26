<script>
    import BtnBanner from './buttons/BannerButton.svelte';
</script>

<div class="banner">
    <div class="content">
        <h1 class="title">Experience Indigo Moon's Magical Shop and Tarot</h1>
        <p class="subtitle">A Spiritual Feeling</p>
    </div>
    <!-- <BtnBanner color='purple' text='Get Started'/> -->
</div>

<style>
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

    @media (max-width: 1000px) {
 
    }
</style>