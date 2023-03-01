<script>
    import BtnBanner from './buttons/BannerButton.svelte';

    $: visibility = 'hidden';
    
    function mobileMenuBtnHandler() {
        visibility === 'hidden' ? visibility = 'visible' : visibility = 'hidden';
    };

    function mobileModalHandler() {
        visibility = 'hidden';
    }
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
    <div class="m__header">
        <div class="m__wrapper-left">
            <h1 class="m__title"><span class="m__indigo">Indigo</span> Moon Tarot</h1>
            <h2 class="m__subtitle">A Spiritual Feeling</h2>
        </div>
        <button class="m__wrapper-right" on:click={mobileMenuBtnHandler}>
            <svg class="m__menu-icon">
                <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
            </svg>
        </button>
    </div>
    <div on:click={mobileModalHandler} class="m__modal-overlay {visibility}"></div>
        <div class="{visibility}">
            <div class="m__menu-modal">
                <h1>In Progress...</h1>
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="cart-icon">
                <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 00-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 00-16.536-1.84M7.5 14.25L5.106 5.272M6 20.25a.75.75 0 11-1.5 0 .75.75 0 011.5 0zm12.75 0a.75.75 0 11-1.5 0 .75.75 0 011.5 0z" />
            </svg>      
            <svg class="icon-test">
                <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
            </svg>
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="home-icon">
                <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 12l8.954-8.955c.44-.439 1.152-.439 1.591 0L21.75 12M4.5 9.75v10.125c0 .621.504 1.125 1.125 1.125H9.75v-4.875c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21h4.125c.621 0 1.125-.504 1.125-1.125V9.75M8.25 21h8.25" />
            </svg>
            <a class="insta-icon" href="https://www.instagram.com/indigomoontarotwithtiffany/" target="_blank" rel="noreferrer">
                <i class="fa-brands fa-instagram"></i>
            </a>
            <a class="yt-icon" href="https://www.youtube.com/@indigomoontarotwithtiffany5535" target="_blank" rel="noreferrer">
                <i class="fa-brands fa-youtube"></i>
            </a>
            <a href="#">About</a>
        </div>
    </div>
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
            display: block;
            position: relative;
        }

        .m__header {
            position: relative;
            z-index: 2;
            padding: 0 1rem;
            color: #fff;
            background-color: #000000e1;
            margin: 0;
            height: 90px;
            gap: 0.5rem;
            
            display: flex;
            text-align: center;
            justify-content: space-between;
            align-items: center;
        }

        .m__wrapper-left {
            text-align: center;
            flex-basis: 100%;
        }

        .m__indigo {
            color: #a782a5;
        }

        .m__title {
            margin: 0;
            padding: 0;
            font-size: 1.5rem;
        }

        .m__subtitle {
            margin: 0;
            padding: 0;
            font-weight: normal;
            font-size: 0.9rem;
        }

        button {
            background: none;
            border: none;
            padding: 0;
            margin: 0;
        }

        .m__modal-overlay {
            z-index: 1;
            background-color: #000000e1;
            background: linear-gradient(to bottom, #351733, #121212ea);
            position: absolute;
            top: 0;
            left: 0;
            height: 100vh;
            width: 100vw;
        }

        .m__menu-modal {
            z-index: 3;
            position: relative;
            background-color: #0000009f;
            color: #fff;
            height: 50vh;
            width: 75vw;
            margin: 5rem auto 0;
            box-shadow: 0 2px 10px #00000056;
            border-radius: 2rem;

            display: grid;
            grid-template-columns: 1fr 1fr;
            justify-content: center;
            align-items: center;
            align-content: center;
            justify-items: center;
        }

        .m__menu-icon {
            stroke: #a782a5;
            stroke-width: 2;
            width: 2rem;
            height: 2rem;
            scale: 1.25;
            border-left: 1px solid #fff;
            padding-left: 0.2rem;
        }
        
        .home-icon {
            stroke: #fff;
            height: 1.5rem;
            width: 1.5rem;
            background-color: green;
        }

        .cart-icon {
            stroke: #fff;
            height: 1.5rem;
            width: 1.5rem;
            background-color: yellow;
        }

        /* Add / Remove classes */
        .visible {
            display: block;
        }

        .hidden {
            display: none;
        }

        .grid {
            display: grid;
        }
    }
</style>