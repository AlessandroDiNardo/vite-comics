<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppContentsCard from './components/AppContentsCard.vue';
import AppFooterSections from './components/AppFooterSections.vue';
import AppFooterInfo from './components/AppFooterInfo.vue';
import AppFooterContacts from './components/AppFooterContacts.vue';

export default {
  name: "App",
  components: {
    AppHeader,
    AppMain,
    AppContentsCard,
    AppFooterSections,
    AppFooterInfo,
    AppFooterContacts
  }
}
</script>

<template>
  <header>
    <AppHeader />
  </header>
  <main>
    <AppMain />
    <AppContentsCard />
  </main>
  <footer>
    <AppFooterSections />
    <AppFooterInfo />
    <AppFooterContacts />
  </footer>
</template>

<style lang="scss">
@use './styles/partials/variables.scss' as *;
@use './styles/general.scss' as *;
</style>
