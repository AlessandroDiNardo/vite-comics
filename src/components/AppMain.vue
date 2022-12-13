<script>
export default {
    name: "AppMain",
}
</script>

<template>
    <section>
        <div class="container">
            <h2> --<span><font-awesome-icon icon="fa-solid fa-angle-right" /></span>
                Content Goes here
                <span><font-awesome-icon icon="fa-solid fa-angle-left" /></span>--
            </h2>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/general.scss' as *;

section {
    background-color: $secondary;
    padding: 30px 0;

    h2 {
        color: white;
    }

    span {
        font-size: 20px;
    }
}
</style>