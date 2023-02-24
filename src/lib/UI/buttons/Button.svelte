<script>
    // JavaScript Below
    export let text;
    export let color;
</script>

<style>
    /* CSS Below */
    .btn:link,
    .btn:visited {
      text-align: center;
    font-size: 1.125rem;
    display: inline-block;
    text-decoration: none;
    border: none;
    color: #fff;
    color: var(--primary);
    padding: 0.75rem 1rem;
    border-radius: 0.5rem;
    margin-bottom: 1.25rem;
    box-shadow: 0 2px 8px #65466492; /* var(--secondary-purple), transparent*/
    box-shadow: 0 2px 8px #fff;
  }
  
  .btn:hover,
  .btn:active {
    cursor: pointer;
    box-shadow: 0 4px 16px #65466464; /* var(--secondary-purple), transparent*/
    scale: 101%;
  }
  
  .btn-purple:link,
  .btn-purple:visited {
    color: #fff;
    background-color: var(--secondary-purple);
  }
  
  .btn-purple:hover,
  .btn-purple:active {
    background-color: #724f71;
  }
</style>

<!-- HTML Below -->
{#if color === 'purple'}
  <a class="btn btn-purple"  href="#">{text}</a>
{/if }