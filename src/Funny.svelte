<script>
    export let fontSize = 100;
    // It's a good practice to set a defaut value for props
    setInterval(() => {
        if (fontSize === 150) {
            fontSize = 5;
        } else {
            fontSize += 1;
        }
    }, 10);
</script>

<h2 style="font-size: {fontSize}px">No soap radio</h2>


