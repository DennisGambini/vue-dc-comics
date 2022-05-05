<template>
    <div class="outer" :style="'background-image: url(' + sfondo + ');'">
        <div class="wrapper">
            
        </div>
    </div>
</template>

<script>
export default {
    name: 'JumboTron',
    props:['sfondo']
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';

.outer{
    height: 300px;
    background-size: cover;
    background-repeat: no-repeat;
}
.wrapper{
    @include wrapper;
}


</style>