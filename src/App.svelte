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

  let alt = "Woman's hands with rings";
  let title1 = "10 min Give it to me straight";
  let title2 = "20 min clarity";
  let title3 = "30 min Psychic Reading";
  let duration1 = "10 min";
  let duration2 = "20 min";
  let duration3 = "30 min";
  let cost1 = "$20";
  let cost2 = "$30";
  let cost3 = "$40";

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
    <h1 class="services-title">Readings</h1>
    <ProductGrid />
  </div>
  <section>
    <div class="container">  
      <Testimonials />
    </div>
  </section>
  <section class="quote-section">
    <Quote />
  </section>
  <section class="video-section container">
    <Video
      title="Unboxing Egyptian Tarot Grand Trumps Deck"
      poster={videoPoster}
      src="../public/unboxing-egyptian.mp4">
	  </Video>
  </section>
  <Map />
  <Footer />
</body>


<style>
  /* CSS Below */
  body {
    position: relative;
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

  .services-title {
    text-align: center;
    font-weight: 400;
    margin: 3rem auto;
  }
</style>