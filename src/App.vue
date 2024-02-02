<script>
import { products, headerLinks, navLinks, footerIcons, linksGroups } from './assets/data';

import AppHeader from './components/AppHeader.vue';
import AppJumbotron from './components/AppJumbotron.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppNav from './components/AppNav.vue';
export default {
    name: 'DC Vite App',
    components: {
        AppHeader,
        AppMain,
        AppFooter,
        AppNav,
        AppJumbotron
    },
    data: () => ({
        products,
        headerLinks,
        navLinks,
        footerIcons,
        linksGroups
    })
}
</script>

<template>
    <AppHeader :links="headerLinks" />
    <AppJumbotron />
    <!-- Jumbotron WIP -->
    <AppMain :products="products" />
    <AppNav :links="navLinks" />
    <AppFooter :icons="footerIcons" :links-groups="linksGroups" />
</template>

<style lang="scss">
@use './assets/scss/style.scss';
</style>