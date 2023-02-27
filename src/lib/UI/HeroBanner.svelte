<script>
    import BtnBanner from './buttons/BannerButton.svelte';

    $: visibility = 'visible';
    
    function mobileMenuHandler(event) {
        let menuButton = document.querySelector('.m__menu-modal');
        console.log(menuButton);
        visibility === 'hidden' ? visibility = 'visible' : visibility = 'hidden'
    };
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
    <div class="m__container">
        <div class="m__wrapper-left">
        <h1 class="m__title"><span class="m__indigo">Indigo</span> Moon Tarot</h1>
        <h2 class="m__subtitle">A Spiritual Feeling</h2>
    </div>
    <button class="m__wrapper-right" on:click={mobileMenuHandler}>
        <svg class="m__menu-icon">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
    </button>
    <div class="m__menu-modal {visibility}">
        <svg class="m__menu-icon">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
        <svg class="icon-test">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
        <svg class="icon-test">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
        <svg class="icon-test">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
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
        }

        .m__container {
            position: relative;
            z-index: 1;
            color: #fff;
            background-color: #000000e1;
            margin: 0;
            height: 90px;
            gap: 0.5rem;
            
            display: flex;
            text-align: center;
            justify-content: space-evenly;
            align-items: center;
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

        button {
            background: none;
            border: none;
            padding: 0;
            margin: 0;
        }

        .m__menu-modal {
            background-color: #000000e1;
            text-transform: uppercase;
            position: absolute;
            top: 90px;
            margin: 0 auto;
            height: 80vh;
            width: 85vw;
            border-radius: 0 0 1rem 1rem;

            display: grid;
            grid-template-columns: 50% auto;
            background-color: red;
            gap: 50px;
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

        .icon-test {
            background-color: blue;
        }

        /* Add / Remove classes */
        .visible {
            display: block;
        }

        .hidden {
            display: none;
        }
    }

</style>