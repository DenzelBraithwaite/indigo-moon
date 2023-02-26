<script>
  // JavaScript Below
  // import Button from './lib/UI/buttons/Button.svelte'
  import ProductGrid from './lib/UI/cards/CardGrid.svelte';
  import Navbar from './lib/UI/navbar.svelte';
  import HeroBanner from './lib/UI/HeroBanner.svelte';
  import Testimonials from './lib/UI/cards/Testimonials.svelte';
  import Quote from './lib/UI/Quote.svelte';
  import Video from './lib/UI/Video.svelte';
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
  let videoPoster = "/video-poster.png";
  
</script>

<body>
  <!-- DESKTOP Below -->
  <div class="desktop">
    <nav>
      <Navbar />
    </nav>
      <header>
        <HeroBanner />
      </header>
      <main>
        <div class="main-container">
          <ProductGrid btnText="Book Now" title="Readings" cards={readingsCards} />
        </div>
        <div class="main-container">  
          <Testimonials />
        </div>
        <div class="main-container">
          <ProductGrid btnText="Buy Now" title="Candles" cards= {candleCards}/>
        </div>
        <Quote />
        <div class="main-container">
          <About />
        </div>
        <div class="main-container">
          <Map />
        </div>
        <!-- <Video
        title="Unboxing Egyptian Tarot Grand Trumps Deck"
        poster={videoPoster}
        src="vids/unboxing-egyptian.mp4">
      </Video> -->
      <footer>
        <Footer />
      </footer>
    </main>
</div>

<!-- MOBILE Below -->
<div class="mobile">

</div>
</body>


<style>
  /* CSS Below */
  body {
    position: relative;
    overflow-x: hidden;
    background: linear-gradient(to bottom, #351733, #4793f76c);
    height: 100vh;
    width: 100vw;
  }

  main {
    background-color: #fffafef3;
    width: 1100px;
    margin: 0 auto;
    transform: translate(0, -100px);
    border-radius: 1rem;
    box-shadow: 0 2px 10px #00000025;
  }

  header {
    position: relative;
  }

  @media (max-width: 1000px) {
    body {
      position: relative;
      overflow-x: hidden;
      background: linear-gradient(to bottom, #351733, #4793f76c);
      height: 100vh;
      width: 100vw;
    }

    main {
      background-color: #fffafef3;
      width: 1100px;
      margin: 0 auto;
      transform: translate(0, -100px);
      border-radius: 1rem;
      box-shadow: 0 2px 10px #00000025;
    }

    header {
      position: relative;
    }
  }
</style>