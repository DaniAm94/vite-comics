<script>
export default {
    name: 'Links Group',
    props: {
        linksGroup: Object
    }
}
</script>

<template>
    <h3>{{ linksGroup.title }}</h3>
    <ul>
        <li v-for="(link, i) in linksGroup.links" :key="i">
            <a href="#">{{ link.text }}</a>
        </li>

    </ul>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/colors' as *;
@use '../../assets/scss/mixins' as *;

h3 {
    color: white;
    text-transform: uppercase;
    margin: 1rem 0;
}

a {
    color: $dc-footer-grey;
}

ul {
    @include flex('column', 'start', 'start');
    row-gap: 0.3rem;
}
</style>