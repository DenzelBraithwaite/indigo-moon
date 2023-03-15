<script>
    import { Link } from 'svelte-routing';

</script>

<!-- Desktop -->
<nav>
    <Link to='/' class="nav-brand"><span class="indigo">Indigo</span> Moon Tarot</Link>
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

<style>
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
    
    :global(.nav-brand:link),
    :global(.nav-brand:visited) {
        text-decoration: none;
        color: #fff;
        font-size: 1.75rem;
        margin: 0;
        font-weight: normal;
        cursor: default;
    }

    :global(.nav-brand:hover),
    :global(.nav-brand:active) {
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
            font-size: 0.9rem;
            gap: 0.65rem;
        }

        :global(.nav-brand:link),
        :global(.nav-brand:visited) {
            font-size: 1rem;
        }
    }

    @media (max-width: 450px) {
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
    }
</style>