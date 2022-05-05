<template>
    

        <div class="wrapper">
            <div class="logo">
                <img src="../assets/images/dc-logo.png" alt="dc logo">
            </div>
            <app-nav :links="allLinks[0].content"/>
        </div>

   
</template>

<script>
import AppNav from './AppNav.vue'

export default {
    name: 'AppHeader',
    components:{
        AppNav
    },
    data(){
        return{
            allLinks: require('../assets/json/FooterLists.json'),
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables';

   .wrapper{
       @include flex-row-between;
       @include wrapper;
       height: 80px;
   }
   .logo{
       height: 80%;
       img{
           height: 100%;
       }
   }
    
</style>