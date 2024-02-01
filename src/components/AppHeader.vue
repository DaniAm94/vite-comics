<script>
export default {
    name: 'App Header',
    data: () => ({

        links: [
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
        activeLinkText: 'Comics'
    }),
    methods: {
        /**
         * it change the current active link whether it's different from the clicked link
         * @param {object} clickedLink the clicked link
         */
        setActiveLink(clickedLink) {
            this.links.forEach(link => {
                if (link.current) link.current = false;
                if (clickedLink.text === link.text) link.current = true;
            })
        }
    }

}
</script>

<template>
    <header>
        <div class="container">

            <figure><img src="../assets/img/dc-logo.png" alt="DC logo"></figure>
            <nav>
                <ul>
                    <li v-for="(link, i) in links" :key="i">
                        <a @click="setActiveLink(link)" href="#" :class="{ active: link.current }">
                            {{ link.text }}
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style scoped>
header {
    height: 130px;
    color: white;
}

header .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

header figure {
    height: 90px;
    width: 90px;
}

ul {
    display: flex;
    column-gap: 1rem;
}

header a {
    color: black;
    font-weight: bold;
    text-transform: uppercase;
    display: block;
    line-height: 130px;
    height: 130px;
}

header a:hover,
header a.active {
    color: hsl(218.76deg 90.82% 61.57%);
    position: relative;
}

header a:hover::after,

header a.active::after {
    content: '';
    height: 4px;
    width: 100%;
    position: absolute;
    left: 0;
    bottom: 0;
    background-color: hsl(218.76deg 90.82% 61.57%);
}
</style>