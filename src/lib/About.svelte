<script>
    // let theme = 'dark-theme';
</script>

<div class="container">
  <h1 class="sub-banner-title">My Background</h1>
  <div class="wrapper">
    <img src="/tiff2.webp" alt="Indigo Moon Tarot Tiffany">
    <div class="content">
      <h2 class="title">A Spiritual Guide</h2>
      <p>Welcome my beautiful peoples, I am a professional Tarot reader and I love, love, love what I do. 
        Everyone seeks advice or guidance at one point or another, I am honored to be a part of your journey. 
        I’m thrilled the stars have brought you here. I’m a successful Tarot Card Reader and magical crafter based 
        in Montreal Quebec - here to guide you through life’s most complex and difficult matters. 
        Whatever you’re going through, I‘m here to help you find your way forward. 
        From a young age I realized I was blessed with a gift that enabled me to see and sense things others could not. 
        Let me do for you what I've done for so many, for over 8 years.
      </p>
    </div>
  </div> 
</div>

<style>
  h1 {
    font-size: 2rem;
    font-weight: normal;
    color: #fff;
    margin-bottom: 4rem;
    color: var(--secondary-purple);
  }
  
  .container {
    text-align: center;
    position: relative;
  }

  .wrapper {
    color: #fff;
    width: 85%;
    margin: 0 auto;

    display: flex;
    align-items: center;
    justify-content: center;
  }

  .content {
    padding: 1rem;
    max-width: 600px;
    border-radius: 1rem;
    background-color: #654664dc; /* Secondary-purple, kept for transparency */
    transform: translate(-10%);
    box-shadow: 0 2px 10px #6546646c;
  }

  .title {
    font-weight: normal;
  }

  img {
    width: 375px;
    border-radius: 1rem;
    box-shadow: 0 2px 10px #65466475;
  }

  p {
    line-height: 1.75rem;
  }

  @media (max-width: 1000px) {
    .wrapper {
      flex-direction: column;
    }

    img {
      width: 320px;
    }

    .content {
      transform: translate(0, -2rem);
    }
  }

  @media (max-width: 450px) {
    /* .wrapper {
      flex-direction: column;
    }

    img {
      width: 320px;
    }

    .content {
      transform: translate(0, -2rem);
    } */
  }
</style>