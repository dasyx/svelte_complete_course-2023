<script>
    import Slider from "./Slider.svelte";
    let redColor = 100;
    let greenColor = 100;
    let blueColor = 100;
</script>


<div class="row">
    <div class="col">
        <h1>Color Picker</h1>
    </div>
</div>
<div class="row">
    <div class="column">
        <form action="">
            <Slider colorName="Red" bind:colorValue={redColor} />
            <Slider colorName="Green" bind:colorValue={greenColor} />
            <Slider colorName="Blue" bind:colorValue={blueColor} />
        </form>
    </div>
</div>
<div class="row">
    <div class="column">
        <div class="color-box" style="background-color: rgb({redColor}, {greenColor}, {blueColor})"></div>
    </div>
</div>
<div class="row">
    <div class="column">
        <p class="color-display">rgb({redColor}, {greenColor}, {blueColor})</p>
    </div>
</div>

<style>
    h1 {
        margin-top: 20px;
    }
    .color-box {
        width: 100%;
        height: 200px;
        border: 3px #fff dashed;
    }
    .color-display {
        text-align: center;
        margin-top: 20px;
    }
</style>