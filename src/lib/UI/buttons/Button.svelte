<script>
  import { Link } from "svelte-routing";

    export let color;
    export let path;
    export let hover;

    // let theme = 'dark-theme';
</script>

{#if color === 'purple'}
  {#if hover === 'blue'}
    <Link class="btn btn-purple blue-hover" to={path}><slot /></Link>
  {/if}

  {#if hover === 'orange'}
    <Link class="btn btn-purple orange-hover" to={path}><slot /></Link>
  {/if}

  {#if hover === 'red'}
    <Link class="btn btn-purple red-hover" to={path}><slot /></Link>
  {/if}

  {#if hover === 'green'}
    <Link class="btn btn-purple green-hover" to={path}><slot /></Link>
  {/if}

  {#if hover === 'purple'}
    <Link class="btn btn-purple purple-hover" to={path}><slot /></Link>
  {/if}

  {#if hover === 'light-purple'}
    <Link class="btn btn-purple light-purple-hover" to={path}><slot /></Link>
  {/if}

  {#if hover === 'indigo'}
    <Link class="btn btn-purple indigo-hover" to={path}><slot /></Link>
  {/if}

  {#if hover === 'yellow'}
    <Link class="btn btn-purple yellow-hover" to={path}><slot /></Link>
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
    min-width: 7rem;
    padding: 0.75rem 1rem;
    border-radius: 0.5rem;
    box-shadow: 0 2px 8px #0000002e;
  }
  
  :global(.btn:hover),
  :global(.btn:active) {
    transition: background-color 0.2s ease-out;
    cursor: pointer;
    box-shadow: 0 2px 10px #0000004d;
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

  :global(.btn-indigo:link),
  :global(.btn-indigo:visited) {
    background: none;
    background-color: #5950A1;
  }
      
  :global(.indigo-hover:hover),
  :global(.indigo-hover:active) {    
    background: none;
    background-color: #7165c7;
  }
     
  :global(.light-purple-hover:hover),
  :global(.light-purple-hover:active) {
    background: none;
    background-color: #aa7bb1;
  }
  :global(.blue-hover:hover),
  :global(.blue-hover:active) {
    background: none;
    background-color: #51a3e6;
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
    background-color: #A3D53E;
  }

  :global(.yellow-hover:hover),
  :global(.yellow-hover:active) {
    background: none;
    background-color: #DCBA13;
  }
  </style>