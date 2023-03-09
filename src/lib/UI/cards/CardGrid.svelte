<script>
  import ProductCard from './ProductCard.svelte';

  export let gridType;
  export let cards = [];
  export let title = '';
  export let btnText = '';

  
  let readingsHovers = [
    'blue',
    'orange',
    'red',
    'green',
    'light-purple',
    'yellow',
  ]

  // Readings Routes
  let readingsLinks = [
    '/candles/yellow',
    '/candles/yellow',
    '/candles/yellow',
  ];

  // Candles
  let candlesLinks = [
    '/candles/yellow',
    '/candles/yellow',
    '/candles/yellow',
    '/candles/yellow',
    '/candles/yellow',
    '/candles/yellow'

  ];
</script>
  
  <h1 class="services-title">{title}</h1>
  <div class="grid">
    {#each cards as card, index}
    <ProductCard
    src={card.src}
    alt={card.alt}
    title={card.title}
    description={card.description}
    cost={card.cost}
    {btnText}
    hover={gridType === 'candles' ? readingsHovers[index] : 'purple'}
    path={gridType === 'readings' ? readingsLinks[index] : candlesLinks[index]}/>
    {/each}
    <a href=# class="m__more">See more</a>
  </div>
  <a href=# class="more">See more</a>
    
<style>
  .m__more {
    display: none;
  }

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
    font-size: 2rem;
  }
  
  .more:link,
  .more:visited {
    text-decoration: none;
    text-align: center;
    display: block;
    color: var(--secondary-purple);
    font-size: 1.8rem;
    margin-top: 2rem;
  }
  
  .more:hover,
  .more:active {
    text-decoration: underline;
  }

  @media (max-width: 1000px) {
    .more:link,
    .more:visited {
      display: none;
    }

    .grid {
      grid-template-columns: 250px;
      row-gap: 5rem;
      justify-content: center;
    }

    .services-title {
      padding-top: 10rem;
    }

    .m__more:link,
    .m__more:visited {
      display: inline-block;
      text-decoration: none;
      padding: 0.5rem 1rem;
      margin: 0 auto;
      border: 2px solid #724f71a1;
      border-radius: 1rem;
      color: #724f71;
      font-size: 1.125rem;
      transform: translate(0, -100%);
    }

    .m__more:active {
      background-color: #724f71;
      color: #fff;
    }
  }
</style>