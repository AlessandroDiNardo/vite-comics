<script>
import ContentCard from "../assets/dc-comics.json"

export default {
    name: "AppContentsCard",
    data() {
        return {
            card: ContentCard
        }
    }
}
</script>

<template>
    <section>
        <div class="container">
            <h2 id="current">CURRENT SERIES</h2>
            <div class="cards-container">
                <div class="cards" v-for="(comic, index) in card" :key="index">
                    <div class="cards-img">
                        <img :src="comic.thumb" alt="">
                    </div>
                    <div class="cards-text">
                        <div>
                            {{ comic.series }}
                        </div>
                        <div class="price">
                            {{ comic.price }}
                        </div>
                        <div>
                            {{ comic.type }}
                        </div>
                    </div>
                </div>
            </div>
            <h2 id="load">LOAD MORE</h2>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/general.scss' as *;

section {
    background-color: $secondary;
    padding: 50px 0;

    .container {
        padding: 50px 0;

        .cards-container {
            width: 100%;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;

            .cards {
                width: calc(100% / 6);
                margin-bottom: 30px;

                .cards-img {
                    width: 100%;

                    img {
                        width: 75%;
                    }
                }

                .cards-text {
                    color: white;
                    line-height: 30px;

                    .price {
                        color: red;
                    }
                }
            }
        }

        #current {
            background-color: $primary;
            width: 300px;
            font-size: 27px;
            text-align: center;
            padding: 10px 15px;
            position: absolute;
            top: 58%;
            left: 10%;

            &:hover {
                cursor: pointer;
                background-color: white;
                color: $primary;
                transition: 1s;
            }
        }

        #load {
            background-color: $primary;
            font-size: 15px;
            text-align: center;
            padding: 10px 15px;
            position: absolute;
            right: 50%;
            border: none;

            &:hover {
                cursor: pointer;
                background-color: rgb(255, 255, 255);
                transition: 1s;
                color: $primary;
            }
        }
    }
}
</style>