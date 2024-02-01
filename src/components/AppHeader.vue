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
        ]
    })

}
</script>

<template>
    <header>
        <div class="container">

            <figure><img src="../assets/img/dc-logo.png" alt="DC logo"></figure>
            <nav>
                <ul>
                    <li v-for="(link, i) in links" :key="i">
                        <a href="#">
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
    min-height: 100px;
    padding: 20px 0;
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
}

header a:hover,
header a.active {
    color: hsl(218.76deg 90.82% 61.57%);
}
</style>