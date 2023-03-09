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
    text-align: center;
    font-size: 1.125rem;
    display: inline-block;
    text-decoration: none;
    border: none;
    color: #fff;
    padding: 0.75rem 1rem;
    border-radius: 0.5rem;
    /* margin-bottom: 1.25rem; */
    box-shadow: 0 2px 8px #65466492; /* var(--secondary-purple), transparent*/
    box-shadow: 0 2px 8px #fff;
  }
  
  :global(.btn:hover),
  :global(.btn:active) {
    cursor: pointer;
    box-shadow: 0 2px 10px #65466438; /* var(--secondary-purple), transparent*/
    scale: 101%;
  }
  
  :global(.btn-purple:link),
  :global(.btn-purple:visited) {
    color: #fff;
    background: linear-gradient(to right, #724f71, #65466492);
  }
      
  :global(.purple-hover:hover),
  :global(.purple-hover:active) {
    background: linear-gradient(to right, #95719b, #65466492);
  }
     
  :global(.light-purple-hover:hover),
  :global(.light-purple-hover:active) {
    background: linear-gradient(to right, #E4B8EB, #65466492);
  }

  :global(.blue-hover:hover),
  :global(.blue-hover:active) {
    background: linear-gradient(to right, #47a8f7e5, #65466492);
  }
  
  :global(.orange-hover:hover),
  :global(.orange-hover:active) {
    background: linear-gradient(to right, #D8690D, #65466492);
  }
    
  :global(.red-hover:hover),
  :global(.red-hover:active) {
    background: linear-gradient(to right, #B92509, #65466492);
  }
    
  :global(.green-hover:hover),
  :global(.green-hover:active) {
    background: linear-gradient(to right, #C3E850, #65466492);
  }

  :global(.yellow-hover:hover),
  :global(.yellow-hover:active) {
    background: linear-gradient(to right, #DCBA13, #65466492);
  }
  </style>