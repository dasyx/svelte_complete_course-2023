<script>
  import Funny from "./Funny.svelte";
  import Test from "./Test.svelte";
  import Fun from "./Fun.svelte";
  let name = "Bob";
  let fontSize = 30;
  let disabled = false;
  setTimeout(() => {
    name = "John";
  }, 1000);
</script>

<!-- <Funny bind:fontSize={size} /> -->
<!-- <Test {name}/> -->
<!-- <Test name="David" /> -->

<h1>Hello Svelte Developer</h1>

<input type="range" bind:value={fontSize} max="1000">
<h3 style="font-size: {fontSize}px">Font Size: {fontSize}px</h3>


<h2>Hello {name}</h2>
<input type="text" bind:value="{name}">
<button disabled={disabled}>Click Me</button>


<style>
  :root {
    background-color: black;
    color: white;
  }

</style>
