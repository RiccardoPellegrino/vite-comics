<template>
    <header>
        <nav class="container">

            <a href="#">
                <img src="../assets/img/dc-logo.png" alt="logoDc">
            </a>

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
        height: 100%;
        line-height: 137px;
        @include dflex;

        li {

            &.active,
            &:hover,
            &:active {
                border-bottom: 3px solid $lightblue;

                a {
                    color: $lightblue;

                }
            }

            a {
                font-size: 16px;
                margin-right: 5px;
                margin-left: 5px;
                font-weight: bold;
                color: black;
                text-decoration: none;
            }
        }
    }
}
</style>