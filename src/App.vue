<template>
  <div id="app">
    <header>
      <app-header/>
    </header>

    <main>
      <jumbo-tron :sfondo="immagineJumbo" />
      <app-grid :lista="dcJson"/>
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
import AppGrid from './components/AppGrid.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppFooter,
    JumboTron,
    AppGrid
  },
  data(){
    return{
      immagineJumbo: require('./assets/images/jumbotron.jpg'),
      dcJson: require('./assets/json/dc-comics.json'),
      
    }
  },
  
}
</script>

<style lang="scss">
  @import './assets/style/generals.scss';

</style>
