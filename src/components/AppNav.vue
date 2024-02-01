<script>
export default {
    name: 'App Nav',
    data: () => ({
        links: [
            {
                icon: 'buy-comics-digital-comics.png',
                text: 'Digital Comics'
            },
            {
                icon: 'buy-comics-merchandise.png',
                text: 'DC Merchandise'
            },
            {
                icon: 'buy-comics-subscriptions.png',
                text: 'Subscription'
            },
            {
                icon: 'buy-comics-shop-locator.png',
                text: 'Comic Shop Locator'
            },
            {
                icon: 'buy-dc-power-visa.svg',
                text: 'Digital Comics'
            }
        ]
    }),
    methods: {
        createImagePath(img) {
            const url = new URL(`../assets/img/${img}`, import.meta.url);
            return url.href;
        }
    }
}
</script>

<template>
    <section id="navigation">
        <div class="container">
            <nav>
                <ul>
                    <li v-for="(link, i) in links" :key="i">
                        <a href="#">
                            <img class="icon" :src="createImagePath(link.icon)" :alt="link.text">
                            {{ link.text }}
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../assets/scss/colors' as *;
@use '../assets/scss/mixins' as *;

#navigation {
    background-color: $dc-blue;
    padding: 40px 0;

    nav {
        padding: 0 50px;
    }

    ul {
        @include flex('', 'between');
    }

    a {
        @include flex();
        color: white;
        column-gap: 1rem;
        text-transform: uppercase;
    }
}


img.icon {
    height: 50px;
    width: auto;
}

li:last-of-type img.icon {
    width: 50px;
    height: auto;
}
</style>