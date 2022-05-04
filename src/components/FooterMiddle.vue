<template>
    <div class="outer">
        <div class="wrapper">

            <ul v-for="(lista, index) in liste" :key="index">
                <li>{{lista.name}}</li>
                <li v-for="(link, indice) in lista.content" :key="indice">
                    {{link.item}}
                </li>
            </ul>

        </div>
    </div>
</template>

<script>
export default {
    name: 'FooterMiddle',
    data(){
        return{
            liste:[
                {
                    name:'DC COMICS',
                    content: [
                        {
                            item: 'Characters',
                            active: true
                        },
                        {
                            item: 'Comics',
                            active: true
                        },
                        {
                            item: 'Movies',
                            active: true
                        },{
                            item: 'Tv',
                            active: true
                        },
                        {
                            item: 'Games',
                            active: true
                        },
                        {
                            item: 'Videos',
                            active: true
                        },
                        {
                            item: 'News',
                            active: true
                        },
                    ]
                },
                {
                    name:'SHOP',
                    content: [
                        {
                            item: 'Shop DC',
                            active: true
                        },
                        {
                            item: 'Shop DC Collectibles',
                            active: true
                        },
                    ]
                },
                {
                    name:'DC',
                    content: [
                        {
                            item: 'Terms Of Use',
                            active: true
                        },
                        {
                            item: 'Privacy Policy (New)',
                            active: true
                        },
                        {
                            item: 'Ad Choices',
                            active: true
                        },{
                            item: 'Advertising',
                            active: true
                        },
                        {
                            item: 'Jobs',
                            active: true
                        },
                        {
                            item: 'Subscriptions',
                            active: true
                        },
                        {
                            item: 'Talent Workshops',
                            active: true
                        },
                        {
                            item: 'CPSC Certificates',
                            active: true
                        },
                        {
                            item: 'Ratings',
                            active: true
                        },
                        {
                            item: 'Shop Help',
                            active: true
                        },
                        {
                            item: 'Contact Us',
                            active: true
                        },
                    ]
                },
                {
                    name:'SITES',
                    content: [
                        {
                            item: 'DC',
                            active: true
                        },
                        {
                            item: 'MAD Magazine',
                            active: true
                        },
                        {
                            item: 'DC Kids',
                            active: true
                        },
                        {
                            item: 'DC Universe',
                            active: true
                        },
                        {
                            item: 'DC Power Visa',
                            active: true
                        },
                    ]
                },
                
            ],
            sfondo: require('../assets/images/footer-bg.jpg')
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables';

    .outer{
        background-image: url('../assets/images/footer-bg.jpg');
    }
    .wrapper{
        height: 300px;
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        justify-content: flex-start;
        align-items: flex-start;
        gap: 30px;
        @include wrapper
    }
    ul{
        @include footer-middle-ul;
    }

</style>