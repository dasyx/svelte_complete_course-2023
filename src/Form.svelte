<script>
    let name = "david";
    let age = 40;
    import { createEventDispatcher } from "svelte";
    // createEventDispatcher returns an object with a dispatch method
    // that we can use to dispatch events
    const dispatch = createEventDispatcher();
    function onSubmit(e) {
        dispatch("submit", {
            name,
            age,
        });
        alert(`Submitted! Name: ${name}, Age: ${age}`);
    }
</script>

<form on:submit|preventDefault={onSubmit}>
    <label for="name">Name</label>
    <input type="text" bind:value={name} id="name" />
    <label for="age">Age</label>
    <input type="number" bind:value={age} id="age" />
    <button type="submit" on:click={onSubmit}>Submit</button>
</form>

<button on:click>Click Me</button>

<style>
    form {
        margin: 20px;
    }
</style>
