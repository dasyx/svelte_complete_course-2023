<script>
    import { createEventDispatcher } from "svelte";
    const dispatch = createEventDispatcher();
  
    function sendColors() {
      dispatch("colors", { color: "blue", backgroundColor: "green" });
    }
  </script>
  
  <button on:click={sendColors}>Envoyer les couleurs au parent</button>
  
  <style>
      div {
          width: 100px;
          height: 100px;
          color: azure;
      }
  </style>
