<script>
export default {
    name: 'Page Footer',
    data: () => ({
        dcComicsLinks: [
            {
                text: 'Characters',
                url: '#',
                current: false,
            },
            {
                text: 'Comics',
                url: '#',
                current: true,
            },
            {
                text: 'Movies',
                url: '#',
                current: false,
            },
            {
                text: 'TV',
                url: '#',
                current: false,
            },
            {
                text: 'Games',
                url: '#',
                current: false,
            },
            {
                text: 'Collectibles',
                url: '#',
                current: false,
            },
            {
                text: 'Videos',
                url: '#',
                current: false,
            },
            {
                text: 'Fans',
                url: '#',
                current: false,
            },
            {
                text: 'News',
                url: '#',
                current: false,
            },
            {
                text: 'Shop',
                url: '#',
                current: false,
            },
        ],
        shopLinks: [
            {
                text: 'Shop DC',
                url: '#',
                current: false,
            },
            {
                text: 'Shop DC collectibles',
                url: '#',
                current: false,
            }
        ],
        dcLinks: [
            {
                text: 'Term Of Use',
                url: '#',
                current: false,
            },
            {
                text: 'Privacy policy (New)',
                url: '#',
                current: false,
            },
            {
                text: 'Ad Choices',
                url: '#',
                current: false,
            },
            {
                text: 'Advertising',
                url: '#',
                current: false,
            },
            {
                text: 'Jobs',
                url: '#',
                current: false,
            },
            {
                text: 'Subscription',
                url: '#',
                current: false,
            },
            {
                text: 'Talent Workshops',
                url: '#',
                current: false,
            },
            {
                text: 'CPSC Certificates',
                url: '#',
                current: false,
            },
            {
                text: 'Ratings',
                url: '#',
                current: false,
            },
            {
                text: 'Shop Help',
                url: '#',
                current: false,
            },
            {
                text: 'Contact Us',
                url: '#',
                current: false,
            },
        ],
        siteLinks: [
            {
                text: 'DC',
                url: '#',
                current: false,
            },
            {
                text: 'MAD Magazine',
                url: '#',
                current: false,
            },
            {
                text: 'DC Kids',
                url: '#',
                current: false,
            },
            {
                text: 'DC Universe',
                url: '#',
                current: false,
            },
            {
                text: 'DC Power Visa',
                url: '#',
                current: false,
            }
        ],
        socials: [
            'footer-facebook.png',
            'footer-twitter.png',
            'footer-youtube.png',
            'footer-pinterest.png',
            'footer-periscope.png'
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
    <footer>
        <div class="footer-top">
            <div class="container">

                <nav class="row">
                    <div class="col">
                        <h3>DC comics</h3>
                        <ul>
                            <li v-for="(link, i) in dcComicsLinks" :key="i">
                                <a href="#">{{ link.text }}</a>
                            </li>

                        </ul>
                        <h3>Shop</h3>
                        <ul>
                            <li v-for="(link, i) in shopLinks" :key="i">
                                <a href="#">{{ link.text }}</a>
                            </li>

                        </ul>
                    </div>
                    <div class="col">
                        <h3>DC</h3>
                        <ul>
                            <li v-for="(link, i) in dcLinks" :key="i">
                                <a href="#">{{ link.text }}</a>
                            </li>

                        </ul>
                    </div>
                    <div class="col">
                        <h3>Sites</h3>
                        <ul>
                            <li v-for="(link, i) in siteLinks" :key="i">
                                <a href="#">{{ link.text }}</a>
                            </li>
                        </ul>
                    </div>
                </nav>
                <figure>
                    <img src="../assets/img/dc-logo-bg.png" alt="">
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
                        <li v-for="social in socials" :key="social">
                            <a href="#">
                                <img :src="createImagePath(social)" alt="facebook logo">
                            </a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </footer>
</template>

<style scoped>
.footer-top {
    background-image: url('../assets/img/footer-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
}

.footer-top .container,
.footer-bottom .container {
    display: flex;
    justify-content: space-between;
    align-items: center;

}

.footer-top .container {
    height: 500px;
    overflow: hidden;
}

.footer-top .row {
    display: flex;
    flex-basis: calc(100% / 3);
    column-gap: 1rem;
}

.footer-top h3 {
    color: white;
    text-transform: uppercase;
    margin: 1rem 0;
}

.footer-top ul {
    display: flex;
    flex-direction: column;
    row-gap: 0.3rem;
}

footer a {
    color: hsl(70.59deg 7.91% 42.16%);
}

.footer-top img {
    width: 600px;
    height: auto;
}

/* Bottom Footer */

.footer-bottom {
    background-color: hsl(0deg 0% 18.82%);
    padding: 2rem 0;
}

#register-btn {
    padding: 15px;
    border: 2px solid hsl(218.76deg 90.82% 61.57%);
    text-transform: uppercase;
    color: white;
}

.footer-bottom ul {
    display: flex;
    align-items: center;
    column-gap: 1rem;
}

.footer-bottom h3 {
    color: hsl(218.76deg 90.82% 61.57%);
    text-transform: uppercase;
}
</style>