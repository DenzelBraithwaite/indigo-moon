<script>

</script>

<nav>
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

<style>
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
        nav {
        position: relative;
        font-family: 'Shantell Sans', 'Mynerve', cursive;
        background-color: #000000d0;
        color: #fff;
        line-height: 1;
        padding: 1rem 1rem;
        margin: 0;
        height: 10vh;

        display: flex;
        text-align: center;
        justify-content: center;
        align-items: center;
    }

    .nav-options {
        display: none;
    }
    }
</style>