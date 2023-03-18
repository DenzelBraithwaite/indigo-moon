<script>
  import Navbar from "../lib/UI/navbar.svelte";
  import HeroBanner from "../lib/UI/HeroBanner.svelte";
  import Footer from "../lib/UI/Footer.svelte";

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
  <img class="product-img" src="/candle-yellow.webp" alt="">
  <div class="product-wrapper-right">
    <h1>Chamomile</h1>
    <h2 class="cost">8$</h2>
    <p class="description">Create a relaxing space and indulge your senses in sweet chamomile.</p>
    <a class="btn btn-purple yellow-hover"  href="mailto:tiffany@indigomoontarot.com">Buy Now</a>
  </div>
</div>
<footer>
  <Footer />
</footer>
           
<style>
  .mobile-nav {
    display: none;
  }

  .product-wrapper {
    position: relative;
    background-color: #ffffff;
    color: #444;
    margin: 8rem auto;
    height: 600px;
    width: 1000px;
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
    color: #DCBA13;
  }

  p {
      padding: 0;
      margin: 0;
  }

  .btn:link,
  .btn:visited {
    display: inline-block;
    text-decoration: none;
    border: none;
    color: #fff;
    width: 70%;
    background-color: #DCBA13;
    text-align: center;
    font-size: 1.125rem;
    padding: 0.75rem 1rem;
    border-radius: 0.5rem;
    margin-bottom: 1.25rem;
    box-shadow: 0 2px 8px #0000001c; /* var(--secondary-purple), transparent*/
  }
  
  .btn:active,
  .btn:hover {
    box-shadow: 0 2px 10px #00000013; /* var(--secondary-purple), transparent*/
    background-color: #ecce38;
  }

  @media (max-width: 450px) {
    .mobile-nav {
      display: block;
    }

    .desktop-nav {
      display: none;
    }

  .product-wrapper {
    margin: 0 auto;
    margin-top: 10rem;
    margin-bottom: 3rem;
    width: 350px;

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
    background-color: #ffffffa1;
    width: 100%;
    height: 100%;
    border-radius: 0 0 1rem 1rem;
    transform: translate(0, -1rem);

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
  }

  }
</style>