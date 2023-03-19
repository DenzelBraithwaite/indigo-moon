<script>
  import { Router, Route, Link } from 'svelte-routing';
  import Home from './routes/home.svelte';
  import BlueCandle from './routes/candles/blueCandle.svelte';
  import OrangeCandle from './routes/candles/orangeCandle.svelte';
  import RedCandle from './routes/candles/redCandle.svelte';
  import GreenCandle from './routes/candles/greenCandle.svelte';
  import PurpleCandle from './routes/candles/purpleCandle.svelte';
  import YellowCandle from './routes/candles/yellowCandle.svelte';
  import StraightReading from './routes/readings/straight.svelte';
  import ClarityReading from './routes/readings/clarity.svelte';
  import PsychicReading from './routes/readings/psychic.svelte';

</script>

<Router>

  <!-- Home -->
  <Route path='/'>
    <Home />
  </Route>

  <!-- Give it to me straight reading -->
  <Route path='readings/straight'>
    <StraightReading />
  </Route>

  <!-- Clarity reading -->
  <Route path='readings/clarity'>
    <ClarityReading />
  </Route>

  <!-- Psychic reading -->
  <Route path='readings/psychic'>
    <PsychicReading />
  </Route>

  <!-- Blue Candle -->
  <Route path="candles/blue">
    <BlueCandle />
  </Route>

  <!-- Orange Candle -->
  <Route path="candles/orange">
    <OrangeCandle />
  </Route>

  <!-- Red Candle -->
  <Route path="candles/red">
    <RedCandle />
  </Route>
  
  <!-- Green Candle -->
  <Route path="candles/green">
    <GreenCandle />
  </Route>
  
  <!-- Purple Candle -->
  <Route path="candles/purple">
    <PurpleCandle />
  </Route>

  <!-- Yellow Candle -->
  <Route path='candles/yellow'>
    <YellowCandle/>
  </Route>
</Router>

<style>
 
</style>