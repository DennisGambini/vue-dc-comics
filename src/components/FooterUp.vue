<template>
    <div class="outer">
        <div class="wrapper">
            <ul>
                <li v-for="(card, index) in cards" :key="index">
                    
                    <img :src="card.image" :alt="card.name">
                    <span>{{card.name}}</span>
                    
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FooterUp',
    data(){
        return{
            cards:[
                {
                    name: 'digital comics',
                    image: require('../assets/images/buy-comics-digital-comics.png'),
                    active: true

                },
                {
                    name: 'dc merchandise',
                    image: require('../assets/images/buy-comics-merchandise.png'),
                    active: true

                },
                {
                    name: 'subscription',
                    image: require('../assets/images/buy-comics-shop-locator.png'),
                    active: true

                },
                {
                    name: 'comic shop locator',
                    image: require('../assets/images/buy-comics-subscriptions.png'),
                    active: true

                },
                {
                    name: 'dc power visa',
                    image: require('../assets/images/buy-dc-power-visa.svg'),
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
        background-color: $blue;
        padding: $section-padding;
    }
    .wrapper{
        @include wrapper;
    }
    ul{
        list-style: none;
        @include flex-row-around;
        li{
            @include flex-row-between;
            gap: 10px;
            color: white;
            text-transform: uppercase;
            font-size: $ul-font-size;
            cursor: pointer;
            border: 1px solid rgba(0,0,0,0);
            border-radius: 5px;
            padding: 6px;
            &:hover{
                background-color: #137bdd;
                border-color: white;
            }
            img{
                height: 45px;
            }
        }
    }

</style>