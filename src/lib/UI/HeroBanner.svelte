<script>
    import BtnBanner from './buttons/BannerButton.svelte';
</script>

<style>
    .banner {
        position: relative;
        background-image: linear-gradient(to bottom, #ffffff17, #00000093),url(../../../public/bg.webp);
        width: 100vw;
        height: 80vh;
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center;

        display: flex;
        align-items: center;
        justify-items: center;
        margin-bottom: 15rem;
    }

    .content {
        color: #fff;
        min-width: 350px;
        width: 50%;
        margin: 0 auto;
        text-align: center;
    }

    .title {
        font-size: 3.75rem;
        line-height: 1.25;
        font-weight: 400;
        text-shadow: 0 2px 20px #000000c4;
    }

    .subtitle {
        font-size: 1.5rem;
        font-weight: lighter;
        text-shadow: 0 2px 10px #ffffff;
    }
</style>

<div class="banner">
    <div class="content">
        <h1 class="title">Experience Indigo Moon's Magical Shop and Tarot</h1>
        <p class="subtitle">A Spiritual Feeling</p>
      </div>
      <BtnBanner color='purple' text='Get Started'/>
</div>