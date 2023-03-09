<script>
  import Navbar from "../lib/UI/navbar.svelte";
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
  
<!-- Desktop -->
<div class="desktop">
  <nav>
    <Navbar />
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
</div>
           
<style>
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
    .desktop {
      display: none;
    }

    .mobile {
      display: block;
    }

    nav {
        display: none;
      }

      nav {
          width: 100vw;
          z-index: 1;
          background-color: #000000ec;
          color: #fff;
          padding: 20px 0;

          position: sticky;
          bottom: 0; 
      }

      .m__header {
          position: relative;
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
  }
</style>