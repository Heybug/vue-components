<template>
    <div id="app">
        <img class="app-img" src="./assets/logo.png">
        <router-view></router-view>
    </div>
</template>

<script>
    export default {
        name: 'app'
    }
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        margin-top: 60px;
    }

    .app-img {
        display: block;
        margin: 0 auto;
    }
</style>
