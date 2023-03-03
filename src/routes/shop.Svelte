<script>
    import Navbar from './lib/UI/navbar.svelte';
    import Footer from './lib/UI/Footer.svelte';
  
    // Videos
    let videoPoster = "/video-poster.webp";
    
  </script>
  
  <body>
    <!-- DESKTOP -->
    <div class="desktop">
      <nav>
        <Navbar />
      </nav>
        <main>
        <footer>
          <Footer />
        </footer>
      </main>
  </div>

 </body>
  
  
  <style>
    body {
      position: relative;
      overflow-x: hidden;
      background: linear-gradient(to bottom, #3b263a 15%, #9f9bbde5, #3b263a);
    }
  
    main {
      background-color: #fffafef3;
      width: 1100px;
      margin: 0 auto;
      transform: translate(0, -100px);
      border-radius: 1rem;
      box-shadow: 0 2px 10px #00000025;
      padding-top: 10rem;
    }
  
    header {
      position: relative;
    }
  
    section {
      margin-bottom: 15rem;
    }
  
    section:last-of-type {
      margin-bottom: 5rem;
    }
  </style>