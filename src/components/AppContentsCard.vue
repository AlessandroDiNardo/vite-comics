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
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/general.scss' as *;

section {
    background-color: $secondary;
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

}
</style>