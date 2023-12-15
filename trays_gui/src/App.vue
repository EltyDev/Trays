<script setup lang="ts">
    import Titlebar from "./components/Titlebar.vue"
    import Window from "./components/Window.vue"
</script>

<template>
    <Titlebar />
    <Window />
    <div id="blur"></div>
</template>

<style scoped>
    #blur {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        backdrop-filter: blur(0.625em);
        z-index: -2;
    }
</style>