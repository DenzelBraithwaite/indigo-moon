<script>
  import { Link } from "svelte-routing";

    export let text;
    export let color;
    export let path;
    export let hover;
</script>

{#if color === 'purple'}
  {#if hover === 'blue'}
    <Link class="link btn btn-purple blue-hover" to={path}>{text}</Link>
  {/if}

  {#if hover === 'orange'}
    <Link class="link btn btn-purple orange-hover" to={path}>{text}</Link>
  {/if}

  {#if hover === 'red'}
    <Link class="link btn btn-purple red-hover" to={path}>{text}</Link>
  {/if}

  {#if hover === 'green'}
    <Link class="link btn btn-purple green-hover" to={path}>{text}</Link>
  {/if}

  {#if hover === 'purple'}
    <Link class="link btn btn-purple purple-hover" to={path}>{text}</Link>
  {/if}

  {#if hover === 'light-purple'}
    <Link class="link btn btn-purple light-purple-hover" to={path}>{text}</Link>
  {/if}

  {#if hover === 'yellow'}
    <Link class="link btn btn-purple yellow-hover" to={path}>{text}</Link>
  {/if}
{/if }

<style>
  :global(.btn),
  :global(.btn:link),
  :global(.btn:visited) {
    transition: background-color 1.25s ease-in;
    text-align: center;
    font-size: 1.125rem;
    display: inline-block;
    text-decoration: none;
    border: none;
    color: #fff;
    padding: 0.75rem 1rem;
    border-radius: 0.5rem;
    box-shadow: 0 2px 8px #65466492; /* var(--secondary-purple), transparent*/
    box-shadow: 0 2px 8px #fff;
  }
  
  :global(.btn:hover),
  :global(.btn:active) {
    transition: background-color 0.2s ease-out;
    cursor: pointer;
    box-shadow: 0 2px 10px #65466438; /* var(--secondary-purple), transparent*/
    scale: 101%;
  }
  
  :global(.btn-purple:link),
  :global(.btn-purple:visited) {
    background: none;
    background-color: #724f71;
  }
      
  :global(.purple-hover:hover),
  :global(.purple-hover:active) {    
    background: none;
    background-color: #95719b;
  }
     
  :global(.light-purple-hover:hover),
  :global(.light-purple-hover:active) {
    background: none;
    background-color: #b689bd;
  }
  :global(.blue-hover:hover),
  :global(.blue-hover:active) {
    background: none;
    background-color: rgba(81, 163, 230, 0.898);
  }
  
  :global(.orange-hover:hover),
  :global(.orange-hover:active) {
    background: none;
    background-color: #D8690D;
  }
    
  :global(.red-hover:hover),
  :global(.red-hover:active) {
    background: none;
    background-color: #c0381c;
  }
    
  :global(.green-hover:hover),
  :global(.green-hover:active) {
    background: none;
    background-color: #C3E850;
  }

  :global(.yellow-hover:hover),
  :global(.yellow-hover:active) {
    background: none;
    background-color: #DCBA13;
  }
  </style>