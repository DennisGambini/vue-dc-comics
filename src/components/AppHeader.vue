<template>
    

        <div class="wrapper">
            <div class="logo">
                <img src="../assets/images/dc-logo.png" alt="dc logo">
            </div>
            <app-nav/>
        </div>

   
</template>

<script>
import AppNav from './AppNav.vue'

export default {
    name: 'AppHeader',
    components:{
        AppNav
    }   
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables';

   .wrapper{
       @include flex-row-between;
       @include wrapper;
   }
    
</style>