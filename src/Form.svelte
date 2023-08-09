<script>
    let name = 'david';
    let age = 40;
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();
    function onSubmit(e) {
        /* alert(`Name: ${name} Age: ${age}`); */
        dispatch('submit', {
            name,
            age
        });
    }
</script>

<form>
    <label for="name">Name</label>
    <input type="text" bind:value={name} id="name">
    <label for="age">Age</label>
    <input type="number" bind:value={age} id="age"> 
    <button type="submit" on:click={onSubmit}>Submit</button>   
</form>

<style>
   form {
       margin: 20px;
   }
</style>