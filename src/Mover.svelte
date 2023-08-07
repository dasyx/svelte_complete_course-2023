<script>
    let x = 0;
    let y = 0;

     function handleKeyup(event) {
        switch (event.key) {
            case "ArrowUp":
                y -= 10;
                break;
            case "ArrowDown":
                y += 10;
                break;
            case "ArrowLeft":
                x -= 10;
                break;
            case "ArrowRight":
                x += 10;
                break;
        }
    }
</script>

<!-- Liez les styles inline pour définir la position de la div -->
<!-- svelte-ignore a11y-no-noninteractive-tabindex -->
<!-- svelte-ignore a11y-no-static-element-interactions -->
<div on:keyup={handleKeyup} tabindex="0" style="left: {x}px; top: {y}px;"></div>


<!-- Ajoutez un style pour visualiser le déplacement de la div -->
<style>
    div {
        width: 50px;
        height: 50px;
        background-color: red;
        position: relative;
    }
</style>
