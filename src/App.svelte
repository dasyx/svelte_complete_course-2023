<script>
   import Container from "./Container.svelte";
   function onFormSubmit(e) {
       console.log(e);
       const { name, age } = e.detail;
       console.log(name, age, 'details from event')
   }

</script>

<Container on:submit={onFormSubmit}/>

<style>
    :root {
        background-color: #fff;
    }
</style>
