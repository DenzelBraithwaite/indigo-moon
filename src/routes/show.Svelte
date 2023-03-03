<script>  
</script>
  
  <body>
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
        <main>
          <div class="product-wrapper">
            <img class="product-img" src="/public/candle-yellow.webp" alt="">
            <div class="product-wrapper-right">
              <h1>Title of Product</h1>
              <p>Other info like cost</p>
              <a class="btn btn-purple yellow-hover"  href="mailto:tiffany@indigomoontarot.com">Request</a>
            </div>
          </div>
          <footer>
            <div class="container">
                <a href="mailto:Indigomoontarotwithtiffany@gmail.com" class="email">Indigomoontarotwithtiffany@gmail.com</a>
                <a href="https://www.instagram.com/indigomoontarotwithtiffany/" class="insta-icon" target="_blank" rel="noreferrer">
                    <i class="insta-icon fa-brands fa-instagram"></i>
                </a>
                <a href="https://www.youtube.com/@indigomoontarotwithtiffany5535" target="_blank" rel="noreferrer">
                    <i class="yt-icon fa-brands fa-youtube"></i>
                </a>
                <p>&copy;2023 by Indigo Moon Tarot</p>
            </div>
        </footer>
      </main>
 </body>
  
  
  <style>
    * {
      box-sizing: border-box;
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
      margin: 2rem auto 0;
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
      box-shadow: 0 2px 20px #00000036;
    }

    .product-wrapper-right {
      box-shadow: 0 2px 20px #00000036;
      background-color: #654664dc;
      background-color: #fffafee7;
      width: 400px;
      height: 500px;
      border-radius: 0 1rem 1rem 0;
      transform: translate(-1rem, 0);

      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-between;
    }

    nav {
      background-color: red;
      position: fixed;
      padding: 10rem;
    }

    body {
      position: relative;
      overflow-x: hidden;
      background: linear-gradient(to bottom, #3b263a 15%, #9f9bbde5, #3b263a);
    }
  
    main {
      width: 1100px;
      background-color: #fffafec0;
      margin: 0 auto;
      transform: translate(0, 100px);
      border-radius: 1rem;
      box-shadow: 0 2px 10px #00000049;
    }

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
      width: 50%;
      background: linear-gradient(to right, #724f71, #65466492);
      text-align: center;
      font-size: 1.125rem;
      padding: 0.75rem 1rem;
      border-radius: 0.5rem;
      margin-bottom: 1.25rem;
      box-shadow: 0 2px 8px #65466492; /* var(--secondary-purple), transparent*/
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
    background: linear-gradient(to right, #DCBA13, #65466492);
  }

    @media (max-width: 1000px) {
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