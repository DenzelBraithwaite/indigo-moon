<script>
  import { Link } from 'svelte-routing';
  import Navbar from "../../lib/UI/navbar.svelte";
  import HeroBanner from "../../lib/UI/HeroBanner.svelte";
  import Footer from "../../lib/UI/Footer.svelte";

  $: visibility = 'hidden';
  
  function mobileMenuBtnHandler() {
      visibility === 'hidden' ? visibility = 'visible' : visibility = 'hidden';
      console.log('testr')
  };

  function mobileModalHandler() {
      visibility = 'hidden';
  }
</script>
  
<!-- Destkop -->
<nav class="desktop-nav">
  <Navbar />
</nav>

<!-- Mobile -->
<nav class="mobile-nav">
  <HeroBanner />
</nav>

<div class="product-wrapper">
  <img class="product-img" src="/candle-blue.webp" alt="">
  <div class="product-wrapper-right">
    <h1>Celestial Blue</h1>
    <h2 class="cost">8$</h2>
    <p class="description">Bergamot - For moon magic or financial manifestation.</p>
    <a class="btn__buy btn-purple blue-hover"  href="mailto:tiffany@indigomoontarot.com">Buy Now</a>
  </div>
</div>
<div class="center">
  <Link on:click={() => {window.history.back()}} class="btn__back" to={'/'}>Back</Link>
</div>
<footer>
  <Footer />
</footer>
           
<style>
  .mobile-nav {
    display: none;
  }

  .center {
    margin: 0 auto 2rem;
    text-align: center;
  }

  .product-wrapper {
    position: relative;
    background-color: #ffffff;
    color: #444;
    margin: 8rem auto 5rem;
    height: 600px;
    width: 950px;
    text-align: center;
    box-shadow: 0px 2px 8px #0000001a;
    border-radius: 1rem;

    display: flex;
    justify-content: center;
    align-items: center;
    gap: 0;
    padding: 0;
  }

  .product-img {
    position: relative;
    height: 100%;
    width: 55%;
    border-radius: 1rem 0 0 1rem;
  }

  .product-wrapper-right {
    width: 45%;
    height: 100%;
    border-radius: 0 1rem 1rem 0;
    /* transform: translate(-2rem, 0); */

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
  }

  .description {
    width: 70%;
  }

  .cost {
    font-size: 3rem;
  }

  p {
      padding: 0;
      margin: 0;
  }

  .btn__buy:link,
  .btn__buy:visited {
    transition: background-color 0.15s ease-in;
    display: inline-block;
    text-decoration: none;
    border: none;
    color: #fff;
    width: 70%;
    background-color: #3e88c5e5;
    text-align: center;
    font-size: 1.125rem;
    padding: 0.75rem 1rem;
    border-radius: 0.5rem;
    margin-bottom: 1.25rem;
    box-shadow: 0 2px 8px #0000001c; /* var(--secondary-purple), transparent*/
  }
  
  .btn__buy:active,
  .btn__buy:hover {
    background-color: #5baceee5;
    box-shadow: 0 2px 10px #00000013; /* var(--secondary-purple), transparent*/
  }

  :global(.btn__back:link),
  :global(.btn__back:visited) {
    transition: background-color 0.1s ease-in;
    display: inline-block;
    text-decoration: none;
    border: none;
    color: #fff;
    width: 200px;
    margin: 0 auto;
    text-align: center;
    background-color: #724f71;
    text-align: center;
    font-size: 1.125rem;
    padding: 0.75rem 1rem;
    border-radius: 0.5rem;
    margin-bottom: 1.25rem;
    box-shadow: 0 2px 8px #0000001c; /* var(--secondary-purple), transparent*/
  }

  :global(.btn__back:hover),
  :global(.btn__back:active) {
    background-color: #95719b;
  }

  @media(max-width: 1000px) {
    .product-wrapper {
    margin: 0 auto;
    margin-top: 10rem;
    margin-bottom: 10rem;
    width: 50%;

    flex-direction: column;
    }

    .product-img {
      height: 100%;
      width: 100%;
      border-radius: 1rem 1rem 0 0;
      box-shadow: 0 2px 20px #00000030;
    }

    .product-wrapper-right {
      box-shadow: 0 2px 20px #00000030;
      width: 100%;
      border-radius: 0 0 1rem 1rem;
      background-color: #fff;

      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-between;
    }

    .btn__buy:link {
      margin: 1.5rem auto;
    }
  }

  @media (max-width: 450px) {
    .mobile-nav {
      display: block;
    }

    .desktop-nav {
      display: none;
    }
  }
</style>