<script>
export default {
    name: "AppMain",
}
</script>

<template>
    <main>
        <div class="container">
            <h2> <span>--<font-awesome-icon icon="fa-solid fa-angle-right" /></span>
                Content Goes here
                <span><font-awesome-icon icon="fa-solid fa-angle-left" />--</span>
            </h2>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/general.scss' as *;

main {
    background-color: $secondary;
    padding: 50px 0;

    h2 {
        color: white;
    }
}
</style>