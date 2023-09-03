<!-- CounterControls.svelte -->
<script>
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();
  
    function increase() {
      dispatch('change', 1);
    }
  
    function decrease() {
      dispatch('change', -1);
    }
  
    function reset() {
      dispatch('reset');
    }
  </script>
  
  <button on:click={increase}>+</button>
  <button on:click={decrease}>-</button>
  <button on:click={reset}>Réinitialiser</button>  