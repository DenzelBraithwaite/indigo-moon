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
    <p class="description">Create a relaxing space and indulge your senses in sweet chamomile.</p>
    <a class="btn btn-purple yellow-hover"  href="mailto:tiffany@indigomoontarot.com">Request</a>
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
    color: #444;
    margin: 8rem auto;
    height: 600px;
    width: 1000px;
    text-align: center;

    display: flex;
    justify-content: center;
    align-items: center;
    gap: 0;
  }

  .product-img {
    position: relative;
    width: 500px;
    height: 500px;
    border-radius: 1rem 0 0 1rem;
    box-shadow: 0 2px 20px #00000030;
  }

  .product-wrapper-right {
    box-shadow: 0 2px 20px #00000030;
    background-color: #654664dc;
    background-color: #ffffffa1;
    width: 400px;
    height: 500px;
    border-radius: 0 1rem 1rem 0;
    transform: translate(-2rem, 0);

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
  }

  .description {
    width: 70%;
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
  }

  @media (max-width: 1000px) {
    .mobile-nav {
      display: block;
    }

    .desktop-nav {
      display: none;
    }
  }
</style>