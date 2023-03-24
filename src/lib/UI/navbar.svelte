<script>
    import { Link } from 'svelte-routing';

    $: visibility = 'hidden';

    function mobileMenuBtnHandler() {
        visibility === 'hidden' ? visibility = 'visible' : visibility = 'hidden';
    };

    function mobileModalHandler() {
        visibility = 'hidden';
    }
</script>

<!-- Desktop -->
<nav>
    <a href="/#" class="nav-brand"><span class="indigo">Indigo</span> Moon Tarot</a>
    <div class="nav-options">
        <a href="/#">Home</a>
        <a href="/#about-section">About</a>
        <a href="/#page-top">Readings</a>
        <a href="/#candle-section">Candles</a>
        <a class="insta-icon" href="https://www.instagram.com/indigomoontarotwithtiffany/" target="_blank" rel="noreferrer">
            <i class="fa-brands fa-instagram"></i>
        </a>
        <a class="yt-icon" href="https://www.youtube.com/@indigomoontarotwithtiffany5535" target="_blank" rel="noreferrer">
            <i class="fa-brands fa-youtube"></i>
        </a>
    </div>
</nav>

<!-- Mobile -->
<div class="mobile">
    <div class="m__header">
        <div class="m__wrapper-left">
            <img class="m__moon" src="/bg.webp" alt="display of tarot cards, candles and sage. Displayed as a circle, resembling a moon.">
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
            <i class="home-icon fa-solid fa-house"></i>
            <i class="cart-icon fa-solid fa-cart-shopping"></i>
            <a class="insta-icon" href="https://www.instagram.com/indigomoontarotwithtiffany/" target="_blank" rel="noreferrer">
                <i class="fa-brands fa-instagram"></i>
            </a>
            <a class="yt-icon" href="https://www.youtube.com/@indigomoontarotwithtiffany5535" target="_blank" rel="noreferrer">
                <i class="fa-brands fa-youtube"></i>
            </a>
        </div>
    </div>
</div>

<style>
    .mobile {
        display: none;
    }
    
    nav {
        font-family: 'Shantell Sans', 'Mynerve', cursive;
        background-color: #000000e7;
        color: #fff;
        line-height: 1;
        width: 100vw;
        padding: 1.25rem 2rem;

        display: flex;
        justify-content: space-between;
        align-items: center;

        position: fixed;
        top: 0;
        z-index: 1;
    }
    
    .nav-brand:link,
    .nav-brand:visited {
        text-decoration: none;
        color: #fff;
        font-size: 1.75rem;
        margin: 0;
        font-weight: normal;
        cursor: default;
    }

    .nav-brand:hover,
    .nav-brand:active {
        cursor: pointer;
        opacity: 0.8;
    }

    .indigo {
        color: #a782a5;
    }

    .nav-options {
        display: flex;
        gap: 2rem;
    }

    .nav-options a:link,
    .nav-options a:visited{
        color: #fff;
        text-decoration: none;
        font-size: 1.25rem;
        display: inline-block;
    }

    .nav-options a:hover,
    .nav-options a:active{
        color: #a782a5;
        cursor: pointer;
    }

    .insta-icon:link,
    .insta-icon:visited,
    .yt-icon:link,
    .yt-icon:visited {
        transition: scale 0.1s ease-out
    }

    .insta-icon:hover,
    .insta-icon:active,
    .yt-icon:hover,
    .yt-icon:active {
        transition: scale 0.2s ease-in;
        scale: 1.5;
    }

    @media (max-width: 1000px) {
        .nav-options {
            display: flex;
            gap: 1rem;
        }
    }

    @media (max-width: 750px) {
        .nav-options,
        .nav-options a:link,
        .nav-options a:visited {
            font-size: 1rem;
            gap: 0.65rem;
        }

        :global(.nav-brand:link),
        :global(.nav-brand:visited) {
            font-size: 1rem;
        }
    }

    @media (max-width: 450px) {
        .desktop {
            display: none;
        }

        .mobile {
            display: block;
            position: relative;
        }

        nav {
            display: none;
        }

        nav {
            z-index: 1;
            background-color: #000000ec;
            color: #fff;
            padding: 20px 0;

            position: sticky;
            bottom: 0; 
        }

        .m__header {
            position: fixed;
            top: 0;
            width: 100vw;
            z-index: 2;
            padding: 1.5rem;
            color: #fff;
            background-color: #000000f5;
            height: 90px;
            
            display: flex;
            align-items: center;
        }
    
        .m__wrapper-left {
            position: relative;
            text-align: center;
            flex-basis: 100%;
        }
        
        .m__indigo {
            color: #a782a5;
        }
        
        .m__moon {
            z-index: 4;
            width: 4rem;
            height: 4rem;
            border-radius: 50%;
            opacity: 50%;
            position: absolute;
            right: 40%;
            top: -10px;
        }
        
        .m__title {
            position: relative;
            z-index: 4;
            margin: 0;
            padding: 0;
            font-size: 1.5rem;
        }

        .m__subtitle {
            position: relative;
            z-index: 4;
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
            background: linear-gradient(to bottom, #2b1b2a, #121212e7);
            position: absolute;
            top: 0;
            left: 0;
            height: 100vh;
            width: 100vw;
        }

        .m__menu-modal {
            z-index: 3;
            position: relative;
            background-color: #000000ad;
            width: 350px;
            height: 350px;
            margin: 5rem auto 0;
            box-shadow: 0 2px 10px #00000056;
            border-radius: 2rem;

            display: grid;
            grid-template-columns: 1fr 1fr;
            grid-template-rows: 1fr 1fr;
            justify-content: center;
            align-items: center;
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
            height: 2.25rem;
            width: 2.25rem;
            color: #000000b0;
            scale: 4;
            background-color: #654664b9;
            border-radius: 5px;

            display: flex;
            justify-content: center;
            align-items: center;
        }

        .cart-icon {
            height: 2.25rem;
            width: 2.25rem;
            color: #000000b0;
            scale: 4;
            background-color: #654664b9;
            border-radius: 5px;

            display: flex;
            justify-content: center;
            align-items: center;
        }

        .insta-icon {
            text-decoration: none;
            height: 2.25rem;
            width: 2.25rem;
            color: #000000b0;
            scale: 4;
            background-color: #654664b9;
            border-radius: 5px;

            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .yt-icon {
            text-decoration: none;
            height: 2.25rem;
            width: 2.25rem;
            color: #000000b0;
            scale: 4;
            background-color: #654664b9;
            border-radius: 5px;

            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* Dynamic classes */
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