<script>
export default {
    name: 'Product Card',
    props: {
        thumb: String,
        series: String
    }
}
</script>

<template>
    <div class="prod-card">
        <figure>
            <img :src="thumb" :alt="series">
        </figure>
        <span>{{ series }}</span>
    </div>
</template>

<style scoped>
.prod-card {
    padding: 0 10px;

    figure {
        width: 183.33px;
        height: 282.03px;
        margin-bottom: 10px;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: center center;
        }
    }

    span {
        text-transform: uppercase;
        font-size: 0.7rem;
    }



}
</style>