<script>
    export let text;
    export let color;
    export let link;
    export let hover;
</script>

{#if color === 'purple'}
  {#if hover === 'blue'}
    <a class="btn btn-purple blue-hover"  href={link}>{text}</a>
  {/if}
  {#if hover === 'orange'}
  <a class="btn btn-purple orange-hover"  href={link}>{text}</a>
  {/if}
  {#if hover === 'red'}
  <a class="btn btn-purple red-hover"  href={link}>{text}</a>
  {/if}
  {#if hover === 'green'}
  <a class="btn btn-purple green-hover"  href={link}>{text}</a>
  {/if}
  {#if hover === 'purple'}
  <a class="btn btn-purple purple-hover"  href={link}>{text}</a>
  {/if}
  {#if hover === 'light-purple'}
  <a class="btn btn-purple light-purple-hover"  href={link}>{text}</a>
  {/if}
  {#if hover === 'yellow'}
  <a class="btn btn-purple yellow-hover"  href={link}>{text}</a>
  {/if}
{/if }

<style>
    .btn:link,
    .btn:visited {
      text-align: center;
      font-size: 1.125rem;
      display: inline-block;
      text-decoration: none;
      border: none;
      color: #fff;
      padding: 0.75rem 1rem;
      border-radius: 0.5rem;
      margin-bottom: 1.25rem;
      box-shadow: 0 2px 8px #65466492; /* var(--secondary-purple), transparent*/
      box-shadow: 0 2px 8px #fff;
  }
  
  .btn:hover,
  .btn:active {
    cursor: pointer;
    box-shadow: 0 2px 10px #65466438; /* var(--secondary-purple), transparent*/
    scale: 101%;
  }
  
  .btn-purple:link,
  .btn-purple:visited {
    color: #fff;
    background-color: var(--secondary-purple);
    background: linear-gradient(to right, #724f71, #65466492);
  }
      
  .purple-hover:hover,
  .purple-hover:active {
    background: linear-gradient(to right, #95719b, #65466492);
  }
     
  .light-purple-hover:hover,
  .light-purple-hover:active {
    background: linear-gradient(to right, #E4B8EB, #65466492);
  }

  .blue-hover:hover,
  .blue-hover:active {
    background: linear-gradient(to right, #47a8f7e5, #65466492);
  }
  
  .orange-hover:hover,
  .orange-hover:active {
    background: linear-gradient(to right, #D8690D, #65466492);
  }
    
  .red-hover:hover,
  .red-hover:active {
    background: linear-gradient(to right, #B92509, #65466492);
  }
    
  .green-hover:hover,
  .green-hover:active {
    background: linear-gradient(to right, #C3E850, #65466492);
  }

  .yellow-hover:hover,
  .yellow-hover:active {
    background: linear-gradient(to right, #DCBA13, #65466492);
  }
  </style>