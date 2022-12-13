<script>
export default {
    name: "AppFooterContacts"
}
</script>

<template>
    <section>
        <div class="container">
            <div class="register-side">
                <button>
                    SIGN UP NOW
                </button>
            </div>
            <div class="socials-side">
                <h2>FOLLOW US</h2>
                <img src="img/footer-facebook.png" alt="">
                <img src="img/footer-periscope.png" alt="">
                <img src="img/footer-pinterest.png" alt="">
                <img src="img/footer-twitter.png" alt="">
                <img src="img/footer-youtube.png" alt="">

            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/variables.scss' as *;

section {
    background-color: $secondary;

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 40px 0;
        z-index: 999;

        .register-side {
            width: 50%;

            button {
                background-color: $secondary;
                border: 3px solid $primary;
                padding: 10px;
                color: white;
                font-size: 17px;
                font-weight: 600;
                cursor: pointer;
            }
        }

        .socials-side {
            width: 50%;
            display: flex;
            justify-content: flex-end;
            gap: 30px;

            h2 {
                color: $primary;
            }
        }
    }
}
</style>