<script>
import AppHeader from './components/AppHeader.vue'
export default {
    name: 'DC Vite App',
    components: {
        AppHeader
    }
}
</script>

<template>
    <div class="container">
        <AppHeader />
    </div>
</template>

<style>
/* Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Generics */
img {
    max-width: 100%;
    height: auto;
    display: block;
}

/* Utils */
.container {
    max-width: 1080px;
    margin: 0 auto;
}
</style>