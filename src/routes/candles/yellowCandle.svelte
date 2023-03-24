<script>
  import { Link } from 'svelte-routing';

  import Navbar from "../../lib/UI/navbar.svelte";
  import Footer from "../../lib/UI/Footer.svelte";
  import BigProductCard from '../../lib/UI/cards/BigProductCard.svelte';

  $: visibility = 'hidden';
  
  function mobileMenuBtnHandler() {
      visibility === 'hidden' ? visibility = 'visible' : visibility = 'hidden';
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
  <Navbar />
</nav>
<BigProductCard
  src="/candle-yellow.webp"
  alt="yellow candle"
  title="Camomile"
  btnText="Buy Now"
  cost="8$"
  description="Create a relaxing space and indulge your senses in sweet chamomile."
  bgColor="yellow"/>
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
    background-color: #232323;
    text-align: center;
    font-size: 1.125rem;
    padding: 0.75rem 1rem;
    border-radius: 0.5rem;
    margin-bottom: 1.25rem;
    box-shadow: 0 2px 8px #0000001c; /* var(--secondary-purple), transparent*/
  }

  :global(.btn__back:hover),
  :global(.btn__back:active) {
    background-color: #3b3b3b;
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