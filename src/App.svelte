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

<!-- ADD ID TO ALL PRODUCTS -->
<!-- ADD ID TO ALL PRODUCTS -->
<!-- ADD ID TO ALL PRODUCTS -->
<!-- ADD ID TO ALL PRODUCTS -->

<Router>
  <!-- Home -->
  <Route path='/' component={Home} />

  <!-- Give it to me straight reading -->
  <Route path='readings/straight' component={StraightReading} />

  <!-- Clarity reading -->
  <Route path='readings/clarity' component={ClarityReading} />

  <!-- Psychic reading -->
  <Route path='readings/psychic' component={PsychicReading} />

  <!-- Blue Candle -->
  <Route path="candles/blue" component={BlueCandle} />

  <!-- Orange Candle -->
  <Route path="candles/orange" component={OrangeCandle} />

  <!-- Red Candle -->
  <Route path="candles/red" component={RedCandle} />
  
  <!-- Green Candle -->
  <Route path="candles/green" component={GreenCandle} />
  
  <!-- Purple Candle -->
  <Route path="candles/purple" component={PurpleCandle} />

  <!-- Yellow Candle -->
  <Route path='candles/yellow' component={YellowCandle} />
</Router>

<style>
 
</style>