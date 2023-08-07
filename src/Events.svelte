<script>
    function clickMe(e) {
        console.log(e.target);
        alert("Clicked");
    }
    function onInput(e) {
        console.log(e, "input");
    }
    function onChange(e) {
        console.log(e, "change");
    }
    function onKeyPressed(e) {
        console.log(e, "key pressed");
    }
    function handleSubmit(e) {
        console.log("handlesubmit");
    }
</script>

<button on:click|once={clickMe}>Click Me</button>
<input type="range" on:input={onInput} on:change={onChange} />
<svelte:window on:keypress={onKeyPressed} />

<form on:submit|stopPropagation|preventDefault={handleSubmit}>
    <button type="submit">Submit Form</button>
</form>
