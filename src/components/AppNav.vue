<template>
    <nav>
        <ul>
            <li v-for="(link, index) in links" :key="index">
                <a href="#">
                    {{link.item}}
                </a>
            </li>
        </ul>
    </nav>
</template>

<script>

export default {
    name: 'AppHeader',
    props: ['links']
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