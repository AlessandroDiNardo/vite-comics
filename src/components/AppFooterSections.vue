<script>
export default {
    name: "AppFooterSections",
    data() {
        return {
            sections: [
                {
                    text: "DIGITAL COMICS",
                    image: "/img/buy-comics-digital-comics.png",
                },
                {
                    text: "DC MERCHANDISE",
                    image: "/img/buy-comics-merchandise.png",
                },
                {
                    text: "SUBSCRIPTION",
                    image: "/img/buy-comics-shop-locator.png",
                },
                {
                    text: "COMIC SHOP LOCATOR",
                    image: "/img/buy-comics-subscriptions.png",
                },
                {
                    text: "DC POWER VISA",
                    image: "/img/buy-dc-power-visa.svg",
                },
            ]
        }
    }
}
</script>

<template>
    <section>
        <div class="container">
            <ul>
                <li v-for="(section, index) in sections" :key="index">
                    <a href="#">
                        <img :src="section.image" alt="">
                        {{ section.text }}
                    </a>
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/general.scss' as *;

section {
    background-color: $primary;
    // debug
    padding: 50px 0;

    ul {
        list-style: none;
        display: flex;
        justify-content: space-around;
        align-items: center;
        gap: 2em;
        font-size: 13px;

        li {
            img {
                width: 20%;
            }

            &:nth-child(n+5) {
                width: 20%;
            }

            a {
                color: rgb(255, 255, 255);
                text-decoration: none;
                font-weight: 700;
                display: flex;
                align-items: center;
                gap: 10px;

                &:hover {
                    text-decoration: 2px underline;
                }
            }
        }

    }
}
</style>