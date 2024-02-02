<script>
import LinksGroup from './links group/LinksGroup.vue';
export default {
    name: 'Page Footer',
    data: () => ({

    }),

    methods: {
        createImagePath(img) {
            const url = new URL(`../assets/img/${img}`, import.meta.url);
            return url.href;
        }
    },
    props: {
        icons: Array,
        linksGroups: Array
    },
    components: {
        LinksGroup
    }

}
</script>

<template>
    <footer>
        <div class="footer-top">
            <div class="container">

                <nav class="links-container">
                    <div v-for="linksGroup in linksGroups" class="links-list">
                        <LinksGroup :linksGroup="linksGroup" />
                    </div>
                </nav>
                <figure>
                    <img src="../assets/img/dc-logo-bg.png" alt="big dc logo">
                </figure>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="container">
                <a href="#" id="register-btn">Sign-Up now!</a>
                <nav>
                    <ul>
                        <li>
                            <h3>Follow us</h3>
                        </li>
                        <li v-for="icon in icons" :key="icon">
                            <a href="#">
                                <img :src="createImagePath(icon)" :alt="icon.text">
                            </a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../assets/scss/colors' as *;
@use '../assets/scss/mixins' as *;

/* Footer generics */
footer {
    .container {
        @include flex('', 'between', )
    }


}

/* Top Footer */
.footer-top {
    background-image: url('../assets/img/footer-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;

    .container {
        height: 600px;
        overflow: hidden;
    }

    .links-container {
        display: flex;
        flex-basis: calc(100% / 3);
        flex-wrap: wrap;

        .links-list {
            flex-basis: calc(100% / 3);
        }
    }

    img {
        width: 700px;
        height: auto;
    }

}



/* Bottom Footer */

.footer-bottom {
    background-color: $dc-dark-grey;
    padding: 2rem 0;

    ul {
        @include flex('', 'start');
        column-gap: 1rem;
    }

    h3 {
        color: $dc-blue;
        text-transform: uppercase;
    }
}

#register-btn {
    padding: 15px;
    border: 2px solid $dc-blue;
    text-transform: uppercase;
    color: white;
}
</style>