<template>
    <div>

        <footer-up/>
        <footer-middle :liste="listeFooter"/>
        <footer-down/>
    </div>
    
</template>

<script>
import FooterUp from './FooterUp.vue';
import FooterMiddle from './FooterMiddle.vue';
import FooterDown from './FooterDown.vue';

export default {
    name: 'AppFooter',
    components:{
        FooterUp,
        FooterMiddle,
        FooterDown
    },
    data(){
        return{
            listeFooter: require('../assets/json/FooterLists.json')
        }
    }
}
</script>

<style lang="scss" scoped>

</style>