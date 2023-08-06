<script>
    let redValue = 0;
    let greenValue = 0;
    let blueValue = 0;
</script>

<main>
    <h1>Color Picker</h1>

    <section class="color-pick-section">
        <p>Red ({redValue})</p>
        <input type="range" bind:value={redValue} max="255"/>

        <p>Green ({greenValue})</p>
        <input type="range" bind:value={greenValue} max="255"/>

        <p>Blue ({blueValue})</p>
        <input type="range" bind:value={blueValue} max="255"/>
    </section>
    <section class="render-section">
        <div style="background-color: rgb({redValue}, {greenValue}, {blueValue})" class="render-section__container" />
            <p>Move the color cursors to change the color</p>
        <div>
        <p>rgb({redValue},{greenValue},{blueValue})</p>
    </section>
</main>

<style>
    main {
        display: flex;
        flex-direction: column;
    }

    main h1 {
        text-align: left;
        margin: 20px 0px 50px 20px;
    }

    .color-pick-section {
        margin-left: 50px;
    }

    .render-section {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .render-section p {
        margin-top: 30px;
        text-align: center;
    }

    .render-section__container {
        border-style: dashed;
        width: 80%;
        height: 350px;
        margin-top: 100px;
    }

    @media (min-width: 1024px) {
        main h1 {
            text-align: center;
        }
        .render-section__container {
            width: 50%;
        }
    }
</style>
