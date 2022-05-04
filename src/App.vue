<template>
  <div id="app">
    <header>
      <app-header/>
    </header>

    <main>
      <app-content/>
    </main>

    <footer>
      <app-footer/>
    </footer>
    
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppContent,
    AppFooter
  }
}
</script>

<style lang="scss">
  @import './assets/style/generals.scss';

</style>
