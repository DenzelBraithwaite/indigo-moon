<script>
    // JavaScript Below
    export let text;
    export let color;
</script>

<style>
    /* CSS Below */
    .btn:link,
    .btn:visited {
    background-color: var(--secondary-purple);
    font-size: 1.5rem;
    text-transform: uppercase;
    display: inline-block;
    text-decoration: none;
    border: none;
    color: #fff;
    padding: 1rem 2rem;
    border-radius: 4px;
    box-shadow: 0 2px 20px #ffffff50;

    position: absolute;
    bottom: 4rem;
    right: 50%;
    transform: translate(50%);
  }
  
  .btn:hover,
  .btn:active {
    cursor: pointer;
    background-color: #714f70;
    box-shadow: 0 2px 25px #ffffff3c;
    scale: 101%;
  }
</style>

<!-- HTML Below -->
<a class="btn"  href="">{text}</a>