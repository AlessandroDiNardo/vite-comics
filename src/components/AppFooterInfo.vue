<script>
export default {
    name: "AppFooterInfo",
    data() {
        return {
            dcComics: [
                {
                    text: "Characters",
                },
                {
                    text: "Comics",
                },
                {
                    text: "Movies",
                },
                {
                    text: "TV",
                },
                {
                    text: "Games",
                },
                {
                    text: "Videos",
                },
                {
                    text: "News",
                },
            ],
            shops: [
                {
                    text: "Shop DC",
                },
                {
                    text: "Shop DC Collectibles"
                },
            ],
            dcs: [
                {
                    text: "Terms Of Use",
                },
                {
                    text: "privacy policy (New)",
                },
                {
                    text: "Ad Choices",
                },
                {
                    text: "Advertising",
                },
                {
                    text: "Jobs",
                },
                {
                    text: "Subscriptions",
                },
                {
                    text: "Talent Workshops",
                },
                {
                    text: "CPSC Certifcates",
                },
                {
                    text: "Ratings",
                },
                {
                    text: "Shop Help",
                },
                {
                    text: "Conact us",
                },
            ],
            sites: [
                {
                    text: "DC",
                },
                {
                    text: "MAD Magazine",
                },
                {
                    text: "DC Kids",
                },
                {
                    text: "DC Universe",
                },
                {
                    text: "DC Power Visa",
                },
            ]
        }
    }
}
</script>

<template>
    <section>
        <div class="container">
            <div class="list">
                <div class="left-side-list">
                    <div class="dcComics">
                        <ul>
                            <h3>DC COMICS</h3>
                            <li v-for="(dcComic, index) in dcComics" :key="index">
                                <a href="#">
                                    {{ dcComic.text }}
                                </a>
                            </li>
                        </ul>
                    </div>
                    <div class="shop">
                        <ul>
                            <h3>SHOP</h3>
                            <li v-for="(shop, index) in shops" :key="index">
                                <a href="#">
                                    {{ shop.text }}
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="right-side-list">
                    <div class="dc">
                        <ul>
                            <h3>DC</h3>
                            <li v-for="(dc, index) in dcs" :key="index">
                                <a href="#">
                                    {{ dc.text }}
                                </a>
                            </li>
                        </ul>
                    </div>
                    <div class="sites">
                        <ul>
                            <h3>SITES</h3>
                            <li v-for="(site, index) in sites" :key="index">
                                <a href="#">
                                    {{ site.text }}
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="logo-bg">
                <img src="img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/general.scss' as *;

section {
    background: url(/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    height: 400px;

    .container {
        display: flex;
        justify-content: space-between;

        .list {
            width: 50%;
            display: flex;
            padding: 50px 0;
            gap: 40px;
            height: 100%;

            .left-side-list {
                display: flex;
                flex-direction: column;
                gap: 20px;
            }

            .right-side-list {
                display: flex;
                flex-direction: row;
                gap: 40px;
            }

            ul {
                list-style: none;

                h3 {
                    margin-bottom: 20px;
                }

                li a {
                    color: grey;
                    font-size: 12px;
                    line-height: 20px;

                    &:hover {
                        text-decoration: underline;
                    }
                }
            }
        }

        .logo-bg {
            width: 50%;
            height: 400px;
            text-align: end;
            overflow: hidden;

            img {
                width: 80%;
            }
        }

    }
}
</style>
