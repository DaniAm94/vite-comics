<script>
import { products } from './assets/data';

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
    },
    data: () => ({
        products
    })
}
</script>

<template>
    <AppHeader />
    <AppMain :products="products" />
    <!-- AppMain updating -->
    <AppNav />
    <AppFooter />
</template>

<style lang="scss">
@use './assets/scss/style.scss';
</style>