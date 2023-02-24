<script>

</script>

<style>
    nav {
        font-family: 'Shantell Sans', 'Mynerve', cursive;
        background-color: #000000a6;
        color: #fff;
        padding: 0.25rem 2rem;
        line-height: 1;
        width: 100vw;

        display: flex;
        justify-content: space-between;
        align-items: center;

        position: absolute;
        top: 0;
        z-index: 1;
    }

    .title {
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
        font-size: 1.125rem;
        display: inline-block;
    }

    .nav-options a:hover,
    .nav-options a:active{
        color: #724F71;
        cursor: pointer;
    }

    .insta-icon:link,
    .insta-icon:visited {
        transition: scale 0.25s ease-out
    }

    .insta-icon:hover,
    .insta-icon:active {
        scale: 1.5;
    }
</style>

<nav>
    <h1 class="title"><span class="indigo">Indigo</span> Moon Tarot</h1>
    <div class="nav-options">
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Book Online</a>
        <a class="insta-icon" href="https://www.instagram.com/indigomoontarotwithtiffany/" target="_blank">
            <i class="fa-brands fa-instagram"></i>
        </a>
    </div>
</nav>