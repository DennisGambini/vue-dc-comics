<template>
    <div class="outer">
        <div class="wrapper">
            <button>sign-up now!</button>
            <div class="footer-dx">
                <span>follow us</span>
                <img v-for="(icon, index) in icone" :key="index" :src="icon.immagine" :alt="icon.name">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FooterDown',
    data(){
        return{
            icone:[
                {
                    name: 'icona facebook',
                    immagine: require('../assets/images/footer-facebook.png'),
                    active: true
                },
                {
                    name: 'icona twitter',
                    immagine: require('../assets/images/footer-twitter.png'),
                    active: true
                },
                {
                    name: 'icona youtube',
                    immagine: require('../assets/images/footer-youtube.png'),
                    active: true
                },
                {
                    name: 'icona pinterest',
                    immagine: require('../assets/images/footer-pinterest.png'),
                    active: true
                },
                {
                    name: 'icona periscope',
                    immagine: require('../assets/images/footer-periscope.png'),
                    active: true
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables';

    .outer{
        background-color: $footer-color;
        padding: 20px 0;
    }
    .wrapper{
        @include wrapper;
        @include flex-row-between;
    }
    button{
        @include btn;
    }
    .footer-dx{
        @include flex-row-between;
        gap: 10px;
        span{
            text-transform: uppercase;
            color: $blue;
        }
        img{
            height: 30px;
        }
    }

</style>