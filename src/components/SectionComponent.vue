<template>

    <main>
        <section>
            <div class="contenitore-init">
                <div class="row ">
                    <div class="card" v-for="(comic, index) in comics" :key="index">
                        <div class="contenitore-img">
                            <img :src="comic.thumb" :alt="comic.series">
                        </div>
                        <div>
                            <h4>{{ comic.series }}</h4>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <div class="btn">
            <button>load more</button>
        </div>

    </main>
</template>

<script>
import { comics } from '../data/data';
export default {
    name: 'SectionComponent',
    data() {
        return {
            comics: comics
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

.contenitore-init {
    margin-top: 10px;
    max-width: 1170px;
    padding: 1rem;
    display: flex;
    justify-content: flex-start;
    margin: 0 auto;

    .row {

        display: flex;
        flex-flow: row wrap;

        .card {
            height: 210px;
            padding: 10px;
            width: calc(100% / 6);

            .contenitore-img {
                height: 90%;
                overflow-y: hidden;

                img {
                    width: 110%;
                }

            }

            div {

                h4 {
                    text-align: center;
                }
            }
        }
    }
}

.btn {

    text-align: center;
    margin-bottom: 10px;

    button {
        background-color: $lightblue;
        height: 40px;
        width: 150px;
        padding: 10px;
        border: 3px solid $lightblue;
        margin-bottom: 10px;
        text-transform: uppercase;
        font-weight: bold;
        color: $lightwhite;
        font-size: 1.2em;
        cursor: pointer;

        &:hover {
            border-radius: 16px;
            background-color: black;

        }
    }
}

section {
    display: flex;
    flex-flow: row nowrap;
    justify-content: center;
    align-items: center;
    justify-content: space-between;

}

main {
    color: $lightwhite;
}
</style>