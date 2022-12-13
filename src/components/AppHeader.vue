<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                },
                {
                    text: "COMICS",
                    url: "#",
                },
                {
                    text: "MOVIES",
                    url: "#",
                },
                {
                    text: "TV",
                    url: "#",
                },
                {
                    text: "GAMES",
                    url: "#",
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                },
                {
                    text: "VIDEOS",
                    url: "#",
                },
                {
                    text: "FANS",
                    url: "#",
                },
                {
                    text: "NEWS",
                    url: "#",
                },
                {
                    text: "SHOP",
                    url: "#",
                },
            ]
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <div class="logo-side">
                <a href="#">
                    <img src="../assets/img/dc-logo.png" alt="">
                </a>
            </div>
            <ul>
                <li v-for="(link, index) in links" :key="index">
                    <a href="#">
                        {{ link.text }}
                    </a>
                </li>
            </ul>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/general.scss' as *;

header {
    background-color: white;

    .container {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    ul {
        list-style: none;
        display: flex;
        justify-content: space-around;
        gap: 2em;
        font-size: 13px;

        li a {
            color: rgb(0, 0, 0);
            font-weight: 600;
            text-decoration: none;

            &.active,
            &:hover {
                color: $primary;
            }
        }
    }
}
</style>