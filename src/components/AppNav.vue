<template>
    <nav>
        <ul>
            <li v-for="(link, index) in links" :key="index">
                {{link.name}}
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

    ul{
        list-style: none;
        @include flex-row-between;
        gap: 20px;
    }

</style>