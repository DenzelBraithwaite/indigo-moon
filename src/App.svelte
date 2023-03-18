<script>
  import { Router, Route, Link } from 'svelte-routing';
  import Home from './routes/home.svelte';
  import BlueCandle from './routes/blueCandle.svelte';
  import OrangeCandle from './routes/orangeCandle.svelte';
  import RedCandle from './routes/redCandle.svelte';
  import GreenCandle from './routes/greenCandle.svelte';
  import PurpleCandle from './routes/purpleCandle.svelte';
  import YellowCandle from './routes/yellowCandle.svelte';

</script>

<Router>

  <!-- Home -->
  <Route path='/'>
    <Home />
  </Route>

  <!-- Blue Candle -->
  <Route path="/candles/blue">
    <BlueCandle />
  </Route>

  <!-- Orange Candle -->
  <Route path="/candles/orange">
    <OrangeCandle />
  </Route>

  <!-- Red Candle -->
  <Route path="/candles/red">
    <RedCandle />
  </Route>
  
  <!-- Green Candle -->
  <Route path="/candles/green">
    <GreenCandle />
  </Route>
  
  <!-- Purple Candle -->
  <Route path="/candles/purple">
    <PurpleCandle />
  </Route>

  <!-- Yellow Candle -->
  <Route path='/candles/yellow'>
    <YellowCandle />
  </Route>
</Router>

<style>
 
</style>