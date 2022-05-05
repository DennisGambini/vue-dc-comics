<template>
    <div class="outer">
        <div class="wrapper">
            <div class="container">

            
                <ul v-for="(lista, index) in liste" :key="index">
                    <li>{{lista.name}}</li>
                    <li v-for="(link, indice) in lista.content" :key="indice">
                        <a href="#">
                        {{link.item}}
                        </a>
                    </li>
                </ul>

            </div>
            <div class="img-wrapper">
                <img src="../assets/images/dc-logo-bg.png" alt="logo sfondo DC">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FooterMiddle',
    props: ['liste']
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables';

    .outer{
        background-image: url('../assets/images/footer-bg.jpg');
        background-size: cover;
        padding: $section-padding;
    }
    .wrapper{
        @include wrapper;
        @include flex-row-between;
    }
    .container{
        height: 250px;
        width: 40%;
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        justify-content: flex-start;
        align-items: flex-start;
        gap: 20px;
    }
    ul{
        @include footer-middle-ul;
    }
    .img-wrapper{
        height: 250px;
        width: 60%;
        overflow: hidden;
        position: relative;
        img{
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            height: 165%;
            z-index: 10;
        }
    }

</style>