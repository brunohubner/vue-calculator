<template>
    <Calculator />
</template>

<script>
import Calculator from "./main/Calculator.vue"
export default {
    components: { Calculator }
}
</script>

<style>
@font-face {
    font-family: "RobotoMono";
    src: url("./fonts/RobotoMono-Thin.ttf");
}

* {
    font-family: RobotoMono, monospace;
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html,
body {
    height: 100%;
}

#app {
    display: flex;
    flex-direction: column;
    height: 100%;
    justify-content: center;
    align-items: center;
    text-align: center;
    color: #fff;
    background-color: #333;
}
</style>
