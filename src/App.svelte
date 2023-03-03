<script>
  import ProductGrid from './lib/UI/cards/CardGrid.svelte';
  import Navbar from './lib/UI/navbar.svelte';
  import HeroBanner from './lib/UI/HeroBanner.svelte';
  import Testimonials from './lib/UI/cards/Testimonials.svelte';
  import Quote from './lib/UI/Quote.svelte';
  // import Video from './lib/UI/Video.svelte';
  import Map from './lib/UI/Map.svelte';
  import Footer from './lib/UI/Footer.svelte';
  import About from './lib/About.svelte';

  // Readings Grid
  let readingsCards = [
      {
        'src': "/reading1.webp",
        'alt': "complete me....",
        'title': "Give it to me straight",
        'description': "10 min",
        'cost': "$20"
      },
      {
        'src': "/reading2.webp",
        'alt': "complete me....",
        'title': "Clarity Reading",
        'description': "20 min",
        'cost': "$30"
      },
      {
        'src': "/reading3.webp",
        'alt': "complete me....",
        'title': "Psychic Reading",
        'description': "30 min",
        'cost': "$40"
      }
    ];

      // Candles Grid
  let candleCards = [
      {
        'src': "/candle-blue.webp", // Try after with symbol, no string?
        'alt': "Blue candle.",
        'title': "Mystical Blue Candle",
        'description': "Experience magical aromas...",
        'cost': "$10"
      },
      {
        'src': "/candle-orange.webp",
        'alt': "orange candle.",
        'title': "Relaxing Orange Candle",
        'description': "Experience magical aromas...",
        'cost': "$10"
      },
      {
        'src': "/candle-red.webp",
        'alt': "red candle.",
        'title': "Passionate Red Candle",
        'description': "Experience magical aromas...",
        'cost': "$10"
      },
      {
        'src': "/candle-yellow.webp",
        'alt': "yellow candle.",
        'title': "Vibrant Yellow Candle",
        'description': "Experience magical aromas...",
        'cost': "$10"
      }
    ];

  // Videos
  let videoPoster = "/video-poster.webp";
  
</script>

<body>
  <!-- DESKTOP -->
  <div class="desktop">
    <nav>
      <Navbar />
    </nav>
      <header>
        <HeroBanner />
      </header>
      <main>
        <section class="main-container">
          <ProductGrid btnText="Book Now" title="Readings" cards={readingsCards} />
        </section>
        <section class="main-container">  
          <Testimonials />
        </section>
        <section class="main-container">
          <ProductGrid btnText="Buy Now" title="Candles" cards= {candleCards}/>
        </section>
        <Quote />
        <section class="main-container">
          <About />
        </section>
        <section class="main-container">
          <Map />
        </section>
        <!-- <Video
        title="Who am I ?"
        poster={videoPoster}
        src="/vids/intro.mp4">
      </Video> -->
      <footer>
        <Footer />
      </footer>
    </main>
</div>

<!-- MOBILE -->
  <div class="mobile">
    <header>
      <HeroBanner />
    </header>
      <main>
        <section class="m__main-container">
          <ProductGrid btnText="Book Now" title="Readings" cards={readingsCards} />
        </section>
        <section class="m__main-container">  
          <Testimonials />
        </section>
        <section class="m__main-container">
          <ProductGrid btnText="Buy Now" title="Candles" cards= {candleCards}/>
        </section>
        <Quote />
        <section class="m__main-container">
          <About />
        </section>
        <section class="map_section m__main-container">
          <Map />
        </section>
      <footer>
        <Footer />
      </footer>
    </main>
    <nav>
      <Navbar />
    </nav>
  </div>
</body>


<style>
  .mobile {
    display: none;
  }

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

  @media (max-width: 1000px) {
    .desktop {
      display: none;
    }

    .mobile {
      display: block;
      margin: 0;
      padding: 0;
    }

    body {
      position: relative;
      overflow-x: hidden;
      background: linear-gradient(to bottom, #3b263a 15%, #9f9bbde5, #3b263a);
      padding-bottom: 10rem; /* Because of main translate 10rem */
    }

    main {
      position: relative;
      background-color: #fffafef3;
      width: 95%;
      margin: 0 auto;
      border-radius: 0;
      box-shadow: 0 2px 10px #00000025;
      transform: translate(0, 8rem);
      border-radius: 1rem;

    }

    header {
      z-index: 1;
      position:fixed;
      top: 0;
      width: 100%;
    }

    nav {
      position: sticky;
      bottom: 0; 
    }
  }
</style>