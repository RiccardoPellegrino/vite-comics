<template>
    <div class="sfondo">
        <div class="container">
            <div class="list-container">
                <DcComponent v-for="(item, index) in menuFooter" :key="index" :obj="item" />
            </div>
            <img src="public/img/dc-logo-bg.png" alt="logo">
        </div>
    </div>
    <div class="socials">
        <div class="container-socials">
            <a href="#nogo" id="sign">sing up now</a>
            <div class="social">
                <span>Follow us</span>
                <img src="../../public/img/footer-facebook.png" alt="fb">
                <img src="../../public/img/footer-twitter.png" alt="twitter">
                <img src="../../public/img/footer-youtube.png" alt="yt">
                <img src="../../public/img/footer-pinterest.png" alt="pinterst">
                <img src="../../public/img/footer-periscope.png" alt="periscope">



            </div>
        </div>

    </div>
</template>

<script>
import { menuFooter } from '../data/data'
import DcComponent from './DcComponent.vue';

export default {
    name: "FooterComponent",
    data() {
        return {
            menuFooter: menuFooter

        };
    },
    components: { DcComponent }
}
</script>

<style lang="scss">
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

.sfondo {
    background-image: url(../../public/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    overflow-y: hidden;


    .container {
        @include dflex;
        height: 370px;

        .list-container {
            display: flex;
            flex-wrap: wrap;

            .list {
                width: calc(100% / 3);

            }

            .list:last-child {
                margin-top: -50px;
            }
        }

        h4 {
            color: $lightwhite;
            text-transform: uppercase;
            font-size: 1.5em;
            margin-bottom: 10px;
        }

        ul {
            color: $lightwhite;
            margin-right: 30px;

            li {
                list-style: none;

                a {
                    color: $bgFooter;
                    ;
                    text-decoration: none;

                    &:hover {
                        color: white;
                    }
                }
            }
        }
    }
}

.container-socials {
    display: flex;
    max-width: 1170px;
    margin: 0 auto;
    padding: 1rem;
    justify-content: space-between;
}

.socials {
    background-color: $bgFooter;
    ;
    padding: 25px;

    a {
        margin-left: -15px;
        border: 3px solid;
        padding: 8px;
        color: $lightwhite;
        text-decoration: none;
        text-transform: uppercase;

        &:hover {
            background-color: $lightblue;
        }
    }

    .social {
        @include dflex;


        span {
            margin-right: 10px;
            color: #1460EA;
            font-size: 2em;
        }

        img {
            margin: 0 10px;

            &:hover {
                filter: brightness(0) invert(1)
            }

        }
    }
}
</style>
