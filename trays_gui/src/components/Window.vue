<script setup lang="ts">
    import Sidebar from "./window/Sidebar.vue"
    import Content from "./window/Content.vue"
</script>

<template>
    <div id="main">
        <Sidebar />
        <Content />
    </div>
</template>

<style scoped>
    #main {
        display: flex;
        flex-direction: row;
        height: 100%;
        width: 100%;
        padding: 0.625em 1.438em; 
        background-color: transparent;
        box-sizing: border-box;
    }
</style>