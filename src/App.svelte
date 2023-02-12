<script>
  // JavaScript Below
  // import Button from './lib/UI/buttons/Button.svelte'
  import Card from './lib/UI/cards/Card.svelte';

  let src1 = "../../../../public/card1.webp";
  let src2 = "../../../../public/card2.webp";
  let src3 = "../../../../public/card3.webp";
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

  .container {
    position: relative;
    width: 80%;
    margin: 0 auto;
  }

  .card-container {
    display: flex;
    gap: 1rem;
  }
</style>

<!-- HTML Below -->
<body>
  <div class="container">
    <div class="card-container">
      <Card
        src={src1}
        alt={alt}
        title={title1}
        duration={duration1}
        cost={cost1}/>
      <Card
        src={src2}
        alt={alt}
        title={title2}
        duration={duration2}
        cost={cost2}/>
      <Card
        src={src3}
        alt={alt}
        title={title3}
        duration={duration3}
        cost={cost3}/>
    </div>

  </div>
</body>