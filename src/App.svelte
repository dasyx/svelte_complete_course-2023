<script>
    //import Container from "./Container.svelte";
    //import Button from "./Button.svelte";
    //import TaskInput from "./TaskInput.svelte";
    //import CounterControls from "./CounterControls.svelte";
    import ThemeSelector from './ThemeSelector.svelte';

    // POUR GEER L'AFFICHAGE DU FORMULAIRE (FORM.SVELTE)

    /*  function onFormSubmit(e) {
        console.log(e);
        const { name, age } = e.detail;
        console.log(name, age, "details from event");
    }
    function onClick() {
        alert("clicked");
    } */

    // POUR GERER L'AFFICHAGE DES COULEURS (BUTTON.SVELTE)

    /* function handleColors(event) {
        $: color = event.detail.color;
        $: backgroundColor = event.detail.backgroundColor;
        console.log(event.detail.color, event.detail.backgroundColor);
    }

    let color = "";
    let backgroundColor = ""; */

    // POUR GERER L'AFFICHAGE DES TACHES (TASKINPUT.SVELTE)

    /* let tasks = [];

    function handleNewTask(event) {
        tasks = [...tasks, event.detail];
    } */

    // POUR GERER L'AFFICHAGE DU COMPTEUR (COUNTER.SVELTE)

    /* let count = 0;

    function handleChange(event) {
        count += event.detail;
    }

    function handleReset() {
        count = 0;
    } */

    // POUR GERER L'AFFICHAGE DU THEME (THEMESELECTOR.SVELTE)

    function handleThemeChange(event) {
    document.body.className = event.detail;
  }
</script>

<!-- <Container on:submit={onFormSubmit} on:click={onClick} /> -->
<!-- <Button on:colors={handleColors} /> -->
<!-- <TaskInput on:newtask={handleNewTask} /> -->

<!-- <div>
    <p>La couleur est : {color}</p>
    <p>La couleur de fond est : {backgroundColor}</p>
</div> -->

<!-- <ul>
    {#each tasks as task (task)}
        <li>{task}</li>
    {/each}
</ul> -->

<!-- <h1>Compteur : {count}</h1>
<CounterControls on:change={handleChange} on:reset={handleReset} /> -->

<ThemeSelector on:themeChange={handleThemeChange} />