<script>
  $: visibility = 'hidden';
  
  function mobileMenuBtnHandler() {
      visibility === 'hidden' ? visibility = 'visible' : visibility = 'hidden';
      console.log('testr')
  };

  function mobileModalHandler() {
      visibility = 'hidden';
  }
</script>
  
<body>
  <!-- Desktop -->
  <div class="desktop">
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
      <div class="product-wrapper">
        <img class="product-img" src="/public/candle-yellow.webp" alt="">
        <div class="product-wrapper-right">
          <h1>Chamomile</h1>
          <p class="description">Create a relaxing space and indulge your senses in sweet chamomile.</p>
          <a class="btn btn-purple yellow-hover"  href="mailto:tiffany@indigomoontarot.com">Request</a>
        </div>
      </div>
      <footer>
        <p class="copyright">&copy;2023 by Indigo Moon Tarot</p>
      </footer>
  </div>
      
  <!-- Mobile -->
  <div class="mobile">
    <div class="mobile">
      <div class="m__header">
        <div class="m__wrapper-left">
          <img class="m__moon" src="/bg.webp" alt="display of tarot cards, candles and sage. Displayed as a circle, resembling a moon.">
          <h1 class="m__title"><span class="m__indigo">Indigo</span> Moon Tarot</h1>
          <h2 class="m__subtitle">A Spiritual Feeling</h2>
        </div>
        <button class="m__wrapper-right" on:click={mobileMenuBtnHandler}>
          <svg class="m__menu-icon">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
          </svg>
        </button>
      </div>
      <div on:click={mobileModalHandler} class="m__modal-overlay {visibility}"></div>
      <div class="{visibility}">
        <div class="m__menu-modal">
          <i class="home-icon fa-solid fa-house"></i>
          <i class="cart-icon fa-solid fa-cart-shopping"></i>
          <a class="insta-icon" href="https://www.instagram.com/indigomoontarotwithtiffany/" target="_blank" rel="noreferrer">
            <i class="fa-brands fa-instagram"></i>
          </a>
          <a class="yt-icon" href="https://www.youtube.com/@indigomoontarotwithtiffany5535" target="_blank" rel="noreferrer">
            <i class="fa-brands fa-youtube"></i>
          </a>
        </div>
      </div>
    </div>
  </div>
</body>
      
        
<style>
  * {
    box-sizing: border-box;
  }

  html {
    background-color: #fff;
    background: linear-gradient(to top, #fff4bd, #fffafe);

  }
  
  .mobile {
    display: none;
  }

  body {
    padding: 0;
    margin: 0;
    font-family: 'Andika', Inter, system-ui, Avenir, sans-serif;
    line-height: 1.5;
    font-weight: 400;

    font-synthesis: none;
    text-rendering: optimizeLegibility;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    -webkit-text-size-adjust: 100%;
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

  nav {
    position: fixed;
    padding: 10rem;
  }

  body {
    position: relative;
    overflow-x: hidden;
  }

  nav {
      font-family: 'Shantell Sans', 'Mynerve', cursive;
      background-color: #000000ec;
      color: #fff;
      line-height: 1;
      width: 100%;
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

  footer{
      text-align: center;
      /* background-color: #271f27; */
      margin: 0 auto;
      padding: 2rem 0;
      color: var(--primary-grey);        
  }
  
  .container {
      width: 70%;
      margin: 0 auto;
  }
  
  .title {
      font-size: 1.5rem;
      font-weight: 400;
      padding: 0;
      margin: 0;
      margin-bottom: 1rem;
  }
  
  .email:visited,
  .email:link {
      display: inline-block;
      font-size: 1rem;
      font-weight: 300;
      text-decoration: none;
      color: var(--primary-grey);
      margin-bottom: 1rem;
  }

  .email:hover,
  .email:active {
      cursor: pointer;
      text-decoration: underline;
      color: var(--secondary-purple);
  }

  .insta-icon,
  .yt-icon {
      color: var(--primary-grey);
      transition: scale 0.25 ease-in;
  }
  
  .insta-icon:hover,
  .insta-icon:active,
  .yt-icon:hover,
  .yt-icon:active {
      transition: scale 0.125s ease-out;
      color: var(--secondary-purple);
      scale: 1.25;
  }

  p {
      padding: 0;
      margin: 0;
  }

  /* Buttons */
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
    box-shadow: 0 2px 8px rgba(101, 70, 100, 0.329); /* var(--secondary-purple), transparent*/
  }
  
  .btn:hover,
  .btn:active {
    cursor: pointer;
    box-shadow: 0 2px 10px #65466438; /* var(--secondary-purple), transparent*/
    scale: 101%;
  }
  
  .btn-purple:link,
  .btn-purple:visited {
    color: #fff;

  }
      
  .purple-hover:hover,
  .purple-hover:active {
    background: linear-gradient(to right, #95719b, #65466492);
  }
     
  .light-purple-hover:hover,
  .light-purple-hover:active {
    background: linear-gradient(to right, #E4B8EB, #65466492);
  }

  .blue-hover:hover,
  .blue-hover:active {
    background: linear-gradient(to right, #47a8f7e5, #65466492);
  }
  
  .orange-hover:hover,
  .orange-hover:active {
    background: linear-gradient(to right, #D8690D, #65466492);
  }
    
  .red-hover:hover,
  .red-hover:active {
    background: linear-gradient(to right, #B92509, #65466492);
  }
    
  .green-hover:hover,
  .green-hover:active {
    background: linear-gradient(to right, #C3E850, #65466492);
  }

  .yellow-hover:hover,
  .yellow-hover:active {
    background-color: #e9c616;
    scale: 1.02;
  }

  .copyright {
    margin: 0;
    padding: 0;
  }

  /* Dynamic classes */
  .visible {
    display: block;
  }

  .hidden {
      display: none;
  }

  .grid {
      display: grid;
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