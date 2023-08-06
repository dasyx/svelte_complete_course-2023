<script>
  import Funny from "./Funny.svelte";
  import Test from "./Test.svelte";
  //let size = 150;
  let name = 'David';
</script>

<!-- <Funny bind:fontSize={size} /> -->
<Test {name}/>

<style>
  :root {
    background-color: black;
    color: white;
  }
</style>
