<script>
  // JavaScript Below
  // import Button from './lib/UI/buttons/Button.svelte'
  import ProductGrid from './lib/UI/cards/CardGrid.svelte';

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
    max-width: 1200px;
    margin: 0 auto;
  }
</style>

<!-- HTML Below -->
<body>
  <div class="container">
      <ProductGrid />
  </div>
</body>