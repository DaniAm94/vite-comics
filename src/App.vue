<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppNav from './components/AppNav.vue';
export default {
    name: 'DC Vite App',
    components: {
        AppHeader,
        AppMain,
        AppFooter,
        AppNav
    }
}
</script>

<template>
    <AppHeader />
    <AppMain />
    <AppNav />
    <AppFooter />
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

ul {
    list-style-type: none;

}

a {
    text-decoration: none;
}

/* Utils */
.container {
    max-width: 1200px;
    margin: 0 auto;
}

body {
    font-family: 'Open Sans Variable', sans-serif;
}
</style>