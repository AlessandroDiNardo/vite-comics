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
  <Header />
</template>

<style lang="scss">
@use './styles/partials/_variables.scss' as *;
@use './styles/general.scss' as *;
</style>
