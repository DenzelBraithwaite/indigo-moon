<script>
  import { Router, Route, Link } from 'svelte-routing';
  import Home from './routes/home.svelte';
  import YellowCandle from './routes/yellowCandle.svelte';

</script>

<Router>

  <!-- Home -->
  <Route path='/'>
    <Home />
  </Route>

  <!-- Yellow Candle -->
  <Route path='/candles/yellow'>
    <YellowCandle />
  </Route>


</Router>

<style>
 
</style>