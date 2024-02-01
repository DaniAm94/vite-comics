<script>
export default {
    name: 'App Header'
}
</script>

<template>
    <header>
        <figure><img src="../assets/img/dc-logo.png" alt="DC logo"></figure>
        <nav>
            <ul>
                <li>
                    <a href="#">
                        Characters
                    </a>
                </li>
                <li>
                    <a href="#">
                        Comics
                    </a>
                </li>
                <li>
                    <a href="#">
                        Movies
                    </a>
                </li>
                <li>
                    <a href="#">
                        Tv
                    </a>
                </li>
                <li>
                    <a href="#">
                        Games
                    </a>
                </li>
                <li>
                    <a href="#">
                        Collectibles
                    </a>
                </li>
                <li>
                    <a href="#">
                        Videos
                    </a>
                </li>
                <li>
                    <a href="#">
                        Fans
                    </a>
                </li>
                <li>
                    <a href="#">
                        News
                    </a>
                </li>
                <li>
                    <a href="#">
                        Shop
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style>
header {
    min-height: 100px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 0;
    color: white;
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