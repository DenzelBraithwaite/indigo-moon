<script>

</script>

<h1>Location</h1>
<a class="map-container" target="_blank" rel="noreferrer" href="https://www.google.com/maps/dir//Montreal,+QC/@45.500415,-73.5713993,15.75z/data=!4m9!4m8!1m0!1m5!1m1!1s0x4cc91a541c64b70d:0x654e3138211fefef!2m2!1d-73.5673919!2d45.5018869!3e0">
  <img class="map-placeholder" src="/map-placeholder.webp" alt="map of montreal area"/>
</a>

<style>
  .map-container{
    width: 100%;
    text-align: center;
  }

  .map-placeholder {
      font-size: 2rem;
      color: var(--primary-grey);
      height: 400px;
      width: 80%;
      max-width: 1000px;
      margin: 0 auto;
      border-radius: 1rem;
      box-shadow: 0 2px 10px #00000028;
      object-fit: cover;
    }

  h1 {
    font-size: 2rem;
    font-weight: normal;
    color: var(--secondary-purple);
    text-align: center;
  }

  a {
    display: inline-block;
  }
  
  @media (max-width: 450px) {
    .map-placeholder {
      font-size: 2rem;
      color: var(--primary-grey);
      height: 300px;
      width: 300px;
      margin: 0 auto;
      border-radius: 1rem;
      box-shadow: 0 2px 10px #00000028;
      object-fit: cover;
    }

    h1 {
      font-size: 2rem;
      font-weight: normal;
      color: var(--secondary-purple);
      text-align: center;
      margin-bottom: 2rem;
    }

    a {
      display: inline-block;
    }
  }
</style>