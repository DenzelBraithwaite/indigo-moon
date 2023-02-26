<script>
    import ProductCard from './ProductCard.svelte';
  
    export let cards = [];
    export let title = '';
    export let btnText = '';
    // export let gridType = '';
  </script>
  
<h1 class="services-title">{title}</h1>
<div class="grid">
    {#each cards as card}
      <ProductCard
        src={card.src}
        alt={card.alt}
        title={card.title}
        description={card.description}
        cost={card.cost}
        {btnText}/>
    {/each}
  </div>
  <a href="#" class="more">See more</a>
    
<style>
  .grid {
    position: relative;
    margin: 0 auto;

    display: grid;
    grid-template-columns: repeat(3, 275px);
    gap: 4rem;
    row-gap: 5rem;
    justify-content: center;
  }
  
  .services-title {
    color: var(--secondary-purple);
    text-align: center;
    font-weight: 400;
    margin: 3rem auto;
    padding-top: 10rem;
    font-size: 2rem;
  }
  
  .more:link,
  .more:visited {
    text-decoration: none;
    text-align: center;
    display: block;
    color: var(--secondary-purple);
    font-size: 1.8rem;
    margin: 5rem auto 15rem;
  }
  
  .more:hover,
  .more:active {
    text-decoration: underline;
  }
</style>