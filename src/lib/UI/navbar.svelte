<script>

</script>

<!-- Desktop -->
<nav class="desktop">
    <h1 class="title"><span class="indigo">Indigo</span> Moon Tarot</h1>
    <div class="nav-options">
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Book Online</a>
        <a class="insta-icon" href="https://www.instagram.com/indigomoontarotwithtiffany/" target="_blank" rel="noreferrer">
            <i class="fa-brands fa-instagram"></i>
        </a>
        <a class="yt-icon" href="https://www.youtube.com/@indigomoontarotwithtiffany5535" target="_blank" rel="noreferrer">
            <i class="fa-brands fa-youtube"></i>
        </a>
    </div>
</nav>

<!-- Mobile -->
<nav class="mobile">
    <div class="m__nav-options">
        <a href="#">About</a>
        <a href="#">
            <svg class="cart-icon">
                <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 00-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 00-16.536-1.84M7.5 14.25L5.106 5.272M6 20.25a.75.75 0 11-1.5 0 .75.75 0 011.5 0zm12.75 0a.75.75 0 11-1.5 0 .75.75 0 011.5 0z" />
              </svg>              
        </a>
        <a href="#">
            <svg class="home-icon">
            <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 12l8.954-8.955c.44-.439 1.152-.439 1.591 0L21.75 12M4.5 9.75v10.125c0 .621.504 1.125 1.125 1.125H9.75v-4.875c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21h4.125c.621 0 1.125-.504 1.125-1.125V9.75M8.25 21h8.25" />
          </svg>
          </a>
        <a class="insta-icon" href="https://www.instagram.com/indigomoontarotwithtiffany/" target="_blank" rel="noreferrer">
            <i class="fa-brands fa-instagram"></i>
        </a>
        <a class="yt-icon" href="https://www.youtube.com/@indigomoontarotwithtiffany5535" target="_blank" rel="noreferrer">
            <i class="fa-brands fa-youtube"></i>
        </a>
    </div>
</nav>

<style>
    .mobile {
        display: none;
    }

    nav {
        font-family: 'Shantell Sans', 'Mynerve', cursive;
        background-color: #000000d0;
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
    
    .title {
        font-size: 1.75rem;
        margin: 0;
        font-weight: normal;
        cursor: default;
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
        .desktop {
            display: none;
        }

        .mobile {
            display: block;
        }

        nav {
            z-index: 1;
            background-color: #000000ec;
            color: #fff;
            padding: 20px 0;

            position: sticky;
            bottom: 0; 
        }

        .home-icon {
            stroke: #fff;
            height: 1.5rem;
            width: 1.5rem;
            stroke-width: 1.5;
        }

        .cart-icon {
            stroke: #fff;
            stroke-width: 1.5;
            height: 1.5rem;
            width: 1.5rem;
        }

        .m__nav-options {
            display: flex;
            justify-content: center;
            gap: 1rem;
        }

        .m__nav-options a:link,
        .m__nav-options a:visited{
            color: #fff;
            text-decoration: none;
            font-size: 1.25rem;
            display: inline-block;
        }

        .m__nav-options a:hover,
        .m__nav-options a:active{
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
    }
</style>