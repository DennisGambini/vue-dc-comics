<template>
  <div id="app">
    <header>
      <app-header/>
    </header>

    <main>
      <jumbo-tron :sfondo="immagineJumbo" />
    </main>

    <footer>
      <app-footer/>
    </footer>
    
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import JumboTron from './components/JumboTron.vue';


export default {
  name: 'App',
  components: {
    AppHeader,
    AppFooter,
    JumboTron
  },
  data(){
    return{
      immagineJumbo: require('./assets/images/jumbotron.jpg')
    }
  }
}
</script>

<style lang="scss">
  @import './assets/style/generals.scss';

</style>
