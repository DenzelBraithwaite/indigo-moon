<script>
    // JavaScript Below
    export let text;
    export let color;
</script>

<style>
    /* CSS Below */
    .btn:link,
    .btn:visited {
    background-color: #654664;
    font-size: 1.125rem;
    display: inline-block;
    text-decoration: none;
    border: none;
    color: #fff;
    padding: 0.75rem 1rem;
    border-radius: 4px;
    margin-bottom: 1rem;
    box-shadow: 0 2px 8px #ffffff95;
  }
  
  .btn:hover,
  .btn:active {
    cursor: pointer;
    background-color: #724f71;
    box-shadow: 0 4px 16px #65466464;
    scale: 101%;
  }
</style>

<!-- HTML Below -->
<a class="btn"  href="#">{text}</a>