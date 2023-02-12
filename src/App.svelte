<script>
  // JavaScript Below
  // import Button from './lib/UI/buttons/Button.svelte'
  import ProductGrid from './lib/UI/cards/CardGrid.svelte';
  import Navbar from './lib/UI/navbar.svelte'
  import HeroBanner from './lib/UI/HeroBanner.svelte'
  import Testimonials from './lib/UI/cards/Testimonials.svelte'

  let src1 = "../../../../card1.webp";
  let src2 = "../../../../card2.webp";
  let src3 = "../../../../card3.webp";
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
  
</script>

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

  .sub-banner {
    position: relative;
    width: 100%;
    height: 60vh;

    display: flex;
  }

  .sub-banner img {
    width: 50%;
    object-fit: cover;
    object-position: center;
  }

  .sub-banner-text-group {
    background-color: #727557;
    color: #fff;
    width: 50%;

    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .content {
    width: 50%;
    margin: 0 auto;
  }

  .sub-banner-title {
    font-size: 2.5rem;
    font-weight: 500;
    line-height: 1;
  }

  .sub-banner-subtitle {
    font-size: 2rem;
    font-weight: lighter;
    line-height: 1;
  }

  .sub-banner-text {
    font-size: 1.5rem;
    font-weight: lighter;
  }
</style>

<!-- HTML Below -->
<body>
  <header>
    <Navbar />
    <HeroBanner />
  </header>
  <section class="sub-banner">
    <img src="../sub_hero_banner.webp" alt="necklace swaying over cards">
    <div class="sub-banner-text-group">
      <div class="content">
        <h1 class="sub-banner-title">My Background</h1>
        <h2 class="sub-banner-subtitle">A Spiritual Guide</h2>
        <p class="sub-banner-text">Welcome, I’m thrilled the stars have brought you here. 
          I’m a successful Tarot Card Reader and magical crafter based 
          in Montreal Quebec - here to guide you through life’s most complex and difficult matters. 
          Whatever you’re going through, I‘m here to help you find your way forward. 
          From a young age I realized I was blessed with a gift that enabled me to see and sense things others could not. 
          Let me do the same for you as I have for so many others since 2015. 
          Contact me to schedule an appointment or phone call reading.</p>
      </div>
    </div>
  </section>
  <Testimonials />
  <div class="container">
      <ProductGrid />
  </div>
</body>