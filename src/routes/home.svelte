<script>
    import { Router, Route, Link } from 'svelte-routing';
  
    import ProductGrid from '../lib/UI/cards/CardGrid.svelte';
    import Navbar from '../lib/UI/navbar.svelte';
    import HeroBanner from '../lib/UI/HeroBanner.svelte';
    import Testimonials from '../lib/UI/cards/Testimonials.svelte';
    import Quote from '../lib/UI/Quote.svelte';
    // import Video from '../lib/UI/Video.svelte';
    import Map from '../lib/UI/Map.svelte';
    import Footer from '../lib/UI/Footer.svelte';
    import About from '../lib/About.svelte';
  
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
        },
      ];
      
        // Candles Grid
    let candleCards = [
        {
          'src': "/candle-blue.webp", // Try after with symbol, no string?
          'alt': "Blue candle.",
          'title': "Celestial Blue",
          'description': "Bergamot - For moon magic or financial manifestation.",
          'cost': "$8"
        },
        {
          'src': "/candle-orange.webp",
          'alt': "Orange candle.",
          'title': "Harvest Spice",
          'description': "Fall time lovers, allow this scent to fill your room, with the sweet fragrances of warm spices and cinnamon. ",
          'cost': "$8"
        },
        {
          'src': "/candle-red.webp",
          'alt': "Red candle.",
          'title': "Red Rose",
          'description': "Bring love and abundance into your life, set an intention and allow your mind to manifest what you desire. ",
          'cost': "$8"
        },
        {
          'src': "/candle-green.webp",
          'alt': "Green candle.",
          'title': "Peppermint & Eucalyptus",
          'description': "Wake up your senses with this fragrant aroma. Perfect for  a bath or morning alertness.",
          'cost': "$8"
        },
        {
          'src': "/candle-purple.webp",
          'alt': "Purple candle.",
          'title': "Lavender",
          'description': "Indulge in a little “ you time “. Have the perfect relaxing evening, preparing for a goodnight rest and sweet dreams.",
          'cost': "$8"
        },
        {
          'src': "/candle-yellow.webp",
          'alt': "yellow candle.",
          'title': "Chamomile",
          'description': "Create a relaxing space and indulge your senses in sweet chamomile.",
          'cost': "$8"
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
            <ProductGrid gridType='readings' btnText="Book Now" title="Readings" cards={readingsCards} />
          </section>
          <section class="main-container">  
            <Testimonials />
          </section>
          <section class="main-container">
            <ProductGrid gridType='candles' btnText="Buy Now" title="Candles" cards= {candleCards}/>
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
            <ProductGrid gridType="readings" btnText="Book Now" title="Readings" cards={readingsCards} />
          </section>
          <section class="m__main-container">  
            <Testimonials />
          </section>
          <section class="m__main-container">
            <ProductGrid gridType="candles" btnText="Buy Now" title="Candles" cards= {candleCards}/>
          </section>
          <Quote />
          <section class="m__main-container">
            <About />
          </section>
          <section class="map-section m__main-container">
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
      width: 90%;
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

    @media (max-width: 450px) {
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
        padding-top: 0;
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
  
      section {
        margin-bottom: 10rem;
      }
    }
  </style>