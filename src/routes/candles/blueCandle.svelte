<script>
  import { Link } from 'svelte-routing';
  import Navbar from "../../lib/UI/navbar.svelte";
  import HeroBanner from "../../lib/UI/HeroBanner.svelte";
  import Footer from "../../lib/UI/Footer.svelte";
  import BigProductCard from '../../lib/UI/cards/BigProductCard.svelte';

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
<BigProductCard
  src="/candle-blue.webp"
  alt="blue candle"
  title="Celestial Blue"
  cost="8$"
  description="Bergamot - For moon magic or financial manifestation."
  bgColor="blue"/>
<div class="center">
  <Link on:click={() => {window.history.back()}} class="btn__back" to='/'>Back</Link>
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

  @media (max-width: 450px) {
    .mobile-nav {
      display: block;
    }

    .desktop-nav {
      display: none;
    }
  }
</style>