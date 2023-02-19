<script>
    // JavaScript Below
    import ProductCard from './ProductCard.svelte';
  
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
    .grid {
      position: relative;
      width: 100%;
      display: grid;
      margin: 0 auto;
      grid-template-columns: repeat(3, 1fr);
      gap: 2rem;
      justify-content: center;
    }
  </style>
  
  <!-- HTML Below -->
<div class="grid">
  <ProductCard
    src={src1}
    alt={alt}
    title={title1}
    duration={duration1}
    cost={cost1}/>
  <ProductCard
    src={src2}
    alt={alt}
    title={title2}
    duration={duration2}
    cost={cost2}/>
  <ProductCard
    src={src3}
    alt={alt}
    title={title3}
    duration={duration3}
    cost={cost3}/>
</div>