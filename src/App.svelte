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
        'src': "bg.webp", // Try after with symbol, no string?
        'alt': "complete me....",
        'title': "Give it to me straight",
        'description': "10 min",
        'cost': "$20"
      },
      {
        'src': "bg.webp",
        'alt': "complete me....",
        'title': "Clarity Reading",
        'description': "20 min",
        'cost': "$30"
      },
      {
        'src': "bg.webp",
        'alt': "complete me....",
        'title': "Psychic Reading",
        'description': "30 min",
        'cost': "$40"
      }
    ];

      // Candles Grid
  let candleCards = [
      {
        'src': "candle-blue.webp", // Try after with symbol, no string?
        'alt': "Blue candle.",
        'title': "Mystical Blue Candle",
        'description': "Experience magical aromas...",
        'cost': "$10"
      },
      {
        'src': "candle-orange.webp",
        'alt': "orange candle.",
        'title': "Relaxing Orange Candle",
        'description': "Experience magical aromas...",
        'cost': "$10"
      },
      {
        'src': "candle-red.webp",
        'alt': "red candle.",
        'title': "Passionate Red Candle",
        'description': "Experience magical aromas...",
        'cost': "$10"
      },
      {
        'src': "candle-yellow.webp",
        'alt': "yellow candle.",
        'title': "Vibrant Yellow Candle",
        'description': "Experience magical aromas...",
        'cost': "$10"
      }
    ];

  // Videos
  let videoPoster = "../public/video-poster.png";
  
</script>

<!-- HTML Below -->
<body>
  <header>
    <Navbar />
    <HeroBanner />
  </header>
  <div class="container">
    <ProductGrid btnText="Book Now" title="Readings" cards={readingsCards} />
  </div>
  <div class="container">
    <ProductGrid btnText="Buy Now" title="Candles" cards= {candleCards}/>
  </div>
  <section>
    <div class="container">  
      <Testimonials />
    </div>
  </section>
  <section class="quote-section">
    <Quote />
  </section>
  <About />
    <!-- <Video
      title="Unboxing Egyptian Tarot Grand Trumps Deck"
      poster={videoPoster}
      src="vids/unboxing-egyptian.mp4">
	  </Video> -->
  <Map />
  <Footer />
</body>


<style>
  /* CSS Below */
  body {
    position: relative;
    overflow-x: hidden;
  }

  header {
    position: relative;
    width: 100vw;
  }

  .container {
    position: relative;
    width: 1200px;
    width: 90vw;
    max-width: 90vw;
    margin: 0 auto;
  }
</style>