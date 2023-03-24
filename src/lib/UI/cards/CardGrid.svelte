<script>
  import ProductCard from './ProductCard.svelte';

  export let gridType;
  export let cards = [];
  export let title = '';
  export let btnText = '';

  
  let candlesHovers = [
    'blue',
    'orange',
    'red',
    'green',
    'light-purple',
    'yellow',
  ]

  let readingsHovers = [
    'purple',
    'purple',
    'purple'
  ];

  // Readings Routes
  let readingsLinks = [
    'readings/straight',
    'readings/clarity',
    'readings/psychic',
  ];

  // Candles
  let candlesLinks = [
    'candles/blue',
    'candles/orange',
    'candles/red',
    'candles/green',
    'candles/purple',
    'candles/yellow'

  ];
</script>
  
{#if gridType === 'readings'}
  <h1 class="services-title">{title}</h1>
  <div class="grid grid__readings">
    {#each cards as card, index}
      <ProductCard
      id="r{index}"
      src={card.src}
      alt={card.alt}
      title={card.title}
      description={card.description}
      cost={card.cost}
      {btnText}
      hover={readingsHovers[index]}
      path={readingsLinks[index]}/>
    {/each}
  </div>

{:else if gridType === 'candles'}
  <h1 class="services-title">{title}</h1>
  <div class="grid grid__candles">
      {#each cards as card, index}
        <ProductCard
        id='c{index}'
        src={card.src}
        alt={card.alt}
        title={card.title}
        description={card.description}
        cost={card.cost}
        {btnText}
        hover={candlesHovers[index]}
        path={candlesLinks[index]}/>
      {/each}
  </div>
{/if}

<style>
  .grid {
    grid-template-columns: repeat(3, 250px);
    position: relative;
    margin: 0 auto;
    display: grid;
    gap: 4rem;
    row-gap: 5rem;
    justify-content: center;
    justify-items: center;
    max-width: 1000px;
  }
  
  .services-title {
    color: var(--secondary-purple);
    text-align: center;
    font-weight: 400;
    font-size: 2rem;
  }
  
  @media (max-width: 1000px) {
    .grid {
      grid-template-columns: auto;
      gap: 4rem;
    }
    
    .services-title {
      font-size: 2rem;
    }
  }

  @media (max-width: 450px) {
    .grid {
      grid-template-columns: 250px;
      row-gap: 5rem;
      justify-content: center;
    }

    .services-title {
      padding-top: 5rem;
    }
  }
</style>