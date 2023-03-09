<script>
  import { Router, Route, Link } from 'svelte-routing';
  import Home from './routes/home.svelte';
  import ShowYellowCandle from './routes/showYellowCandle.svelte';

</script>

<Router>

  <!-- Home -->
  <Route path='/'>
    <Home />
  </Route>

  <!-- Yellow Candle -->
  <Route path='/candles/yellow'>
    <ShowYellowCandle />
  </Route>


</Router>

<style>
  .mobile {
    display: none;
  }

  body {
    position: relative;
    overflow-x: hidden;
    background: linear-gradient(to bottom, #3b263a 15%, #9f9bbde5, #3b263a);
  }

  main {
    background-color: #fffafef3;
    width: 1100px;
    margin: 0 auto;
    transform: translate(0, -100px);
    border-radius: 1rem;
    box-shadow: 0 2px 10px #00000025;
    padding-top: 10rem;
  }

  header {
    position: relative;
  }

  section {
    margin-bottom: 15rem;
  }

  section:last-of-type {
    margin-bottom: 5rem;
  }

  @media (max-width: 1000px) {
    .desktop {
      display: none;
    }

    .mobile {
      display: block;
      margin: 0;
      padding: 0;
    }

    body {
      position: relative;
      overflow-x: hidden;
      background: linear-gradient(to bottom, #3b263a 15%, #9f9bbde5, #3b263a);
      padding-bottom: 10rem; /* Because of main translate 10rem */
    }

    main {
      position: relative;
      background-color: #fffafef3;
      width: 95%;
      margin: 0 auto;
      border-radius: 0;
      box-shadow: 0 2px 10px #00000025;
      transform: translate(0, 8rem);
      border-radius: 1rem;
      padding-top: 0;
    }

    header {
      z-index: 1;
      position:fixed;
      top: 0;
      width: 100%;
    }

    nav {
      position: sticky;
      bottom: 0; 
    }

    section {
      margin-bottom: 10rem;
    }
  }
</style>