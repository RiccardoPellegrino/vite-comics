<template>
    <section class="blue">
        <div class="conteiner">
            <ul>
                <li v-for="(item, index) in blueimg" key:="index">
                    <a :href="item.url">
                        <img :src="item.img" :alt="item.text">
                        <span>{{ item.text }}</span>
                    </a>

                </li>
            </ul>
        </div>
    </section>
</template>

<script>
export default {
    name: 'IconComponent',
    data() {
        return {
            blueimg: [
                {
                    url: "#nogo",
                    img: "/public/img/buy-comics-digital-comics.png",
                    text: "Digital Comics"
                },
                {
                    url: "#nogo",
                    img: "/public/img/buy-comics-merchandise.png",
                    text: "Dc Merchandise"
                },
                {
                    url: "#nogo",
                    img: "/public/img/buy-comics-subscriptions.png",
                    text: "Subscriptions"
                },
                {
                    url: "#nogo",
                    img: "/public/img/buy-comics-shop-locator.png",
                    text: "Comics Shop locator"
                },

                {
                    url: "#nogo",
                    img: "/public/img/buy-dc-power-visa.svg",
                    text: "Dc power Visa"
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

.blue {
    background-color: $lightblue;

    .conteiner {
        color: white;
        padding-top: 40px;
        padding-bottom: 40px;

        ul {
            @include dflex;

            li {
                list-style: none;
                margin-right: 10px;

                a {
                    @include dflex;
                    color: $lightwhite;
                    text-decoration: none;

                    img {
                        width: 50px;


                    }

                    span {
                        margin-left: 8px;
                        text-transform: uppercase;
                    }
                }
            }
        }
    }
}
</style>