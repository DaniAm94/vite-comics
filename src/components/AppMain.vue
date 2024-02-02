<script>
import ProductCard from './products/ProductCard.vue';
export default {
    name: 'App Main',
    props: {
        products: Array
    },
    components: {
        ProductCard,
    }
}
</script>

<template>
    <main>
        <section id="products">
            <div class="container">
                <h2>Current Series</h2>
                <div class="card-container">
                    <ProductCard v-for="product in products" :key="product.series" :thumb="product.thumb"
                        :series="product.series" />
                </div>
                <button role="button" id="load-btn">Load More</button>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/scss/colors' as*;

main {
    background-color: $dc-black;
    min-height: 100px;
    color: white;
    padding: 50px 0;

    .container {
        position: relative;
    }

    #products h2 {
        background-color: $dc-blue;
        width: auto;
        padding: 5px 15px;
        position: absolute;
        top: -70px;
        left: 0;

    }

    .card-container {
        display: flex;
        flex-wrap: wrap;
        row-gap: 2rem;
        margin: 0 -10px;
    }

    .prod-card {
        flex-basis: calc(100% / 6);
    }
}

#load-btn {
    color: white;
    background-color: $dc-blue;
    border: none;
    border-radius: 5px;
    padding: 5px 30px;
    margin: 10px auto;
    display: block;
    cursor: pointer;
    text-transform: uppercase;
}
</style>