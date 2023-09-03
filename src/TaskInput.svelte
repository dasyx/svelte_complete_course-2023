<!-- TaskInput.svelte -->
<script>
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();
  
    let task = "";
  
    function addTask() {
      dispatch('newtask', task);
      task = ""; // réinitialiser l'input
    }
  </script>
  
  <input bind:value={task} placeholder="Entrez une nouvelle tâche" />
  <button on:click={addTask}>Ajouter</button>