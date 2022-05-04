<template>
    <nav>
        <ul>
            <li v-for="(link, index) in links" :key="index">
                <a href="#">
                    {{link.name}}
                </a>
            </li>
        </ul>
    </nav>
</template>

<script>

export default {
    name: 'AppHeader',
    data(){
        return{
            links:[
                {
                    name: 'characters',
                    active: true
                },
                {
                    name: 'comics',
                    active: false
                },
                {
                    name: 'movies',
                    active: false
                },
                {
                    name: 'tv',
                    active: false
                },
                {
                    name: 'games',
                    active: false
                },
                {
                    name: 'collectibles',
                    active: false
                },
                {
                    name: 'videos',
                    active: false
                },
                {
                    name: 'fans',
                    active: false
                },
                {
                    name: 'news',
                    active: false
                },
                {
                    name: 'shop',
                    active: false
                },
            ]
        }
    }   
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables';

    *{
        text-transform: uppercase;
    }
    nav{
        height: 100%;
    }
    ul{
        @include flex-row-between;
        height: 100%;
        list-style: none;
        gap: 20px;
        font-size: $ul-font-size;
        font-weight: $ul-font-weight;
        
        li{
            height: 100%;
            cursor: pointer;
            
            &:hover{
                a{
                    color: $blue;
                }
                border-bottom: 3px solid $blue;
            }
            a{
                color: $footer-color;
                display: block;
                padding-top: 32px;
            }
        }
    }

</style>