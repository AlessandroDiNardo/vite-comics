<script>
import Header from './components/Header.vue';

export default {
  name: "App",
  components: {
    Header
  }
}
</script>

<template>
  <div class="container">
    <Header />
  </div>
</template>

<style lang="scss">
@use './styles/partials/variables.scss' as *;
@use './styles/general.scss' as *;
</style>
