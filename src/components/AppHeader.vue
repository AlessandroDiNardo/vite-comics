<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: "false",
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: "false",
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: "false",
                },
                {
                    text: "TV",
                    url: "#",
                    current: "false",
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: "false",
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: "false",
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: "false",
                },
                {
                    text: "FANS",
                    url: "#",
                    current: "false",
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: "false",
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: "false",
                },
            ]
        }
    }
}
</script>

<template>
    <section>
        <div class="container">
            <div class="logo-side">
                <a href="#">
                    <img src="/img/dc-logo.png" alt="">
                </a>
            </div>
            <div>
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a href="#" :class="{ active: links.current }">
                            {{ link.text }}
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/general.scss' as *;

section {
    background-color: white;

    .container {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding-top: 20px;

        .logo-side {
            height: 100%;

            img {
                width: 90%;
            }
        }

        ul {
            list-style: none;
            display: flex;
            justify-content: space-around;
            align-items: center;
            gap: 2em;
            font-size: 13px;

            li a {
                color: rgb(0, 0, 0);
                font-weight: 700;
                text-decoration: none;
                display: flex;
                align-items: center;
                height: 110px;

                &.active,
                &:hover {
                    color: $primary;
                    border-bottom: 4px solid $primary;
                }
            }
        }
    }
}
</style>