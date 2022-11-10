<template>
    <header>
        <nav class="container">
            <div class="logo">
                <a href="#">
                    <img src="../assets/img/dc-logo.png" alt="logoDc">
                </a>
            </div>
            <ul>
                <li v-for="(link, index) in links" :key="index">
                    <a :href="link.url" :class="{ 'active': link.current }">{{ link.text }}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {
    name: 'NavComponent',
    data() {
        return {
            links: [
                {
                    text: "Characters",
                    url: "#",
                    current: false,
                },
                {
                    text: "Comics",
                    url: "#",
                    current: true,
                },
                {
                    text: "Movies",
                    url: "#",
                    current: false,
                },
                {
                    text: "TV",
                    url: "#",
                    current: false,
                },
                {
                    text: "Games",
                    url: "#",
                    current: false,
                },
                {
                    text: "Collectibles",
                    url: "#",
                    current: false,
                },
                {
                    text: "Videos",
                    url: "#",
                    current: false,
                },
                {
                    text: "Fans",
                    url: "#",
                    current: false,
                },
                {
                    text: "News",
                    url: "#",
                    current: false,
                },
                {
                    text: "Shop",
                    url: "#",
                    current: false,
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

header {
    text-align: center;
    width: 100%;
    background-color: $lightwhite;
    height: 140px;


    nav {
        @include dflex;
        justify-content: space-between;
        height: 100%;
    }

    ul {
        list-style: none;
        line-height: 100px;

        @include dflex;

        li a {
            height: 100px;
            display: inline-block;
            padding: 0 1rem;
            text-decoration: none;
            font-weight: 550;
            color: $lightblack;
            transition: background 0.3s;



            &.active {
                border-bottom: 1px solid blue;
            }

            &:hover {
                color: lighten($lightblue, 40%);
            }
        }
    }
}
</style>