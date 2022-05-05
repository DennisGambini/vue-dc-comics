<template>
    <div class="outer">
        <h2>current series</h2>
        <div class="wrapper">
            <div v-for="(item, index) in lista" :key="index" class="card">
                <div class="price">{{item.price}}</div>
                <img :src="item.thumb" :alt="item.series">
                <div>{{item.series}}</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AppGrid',
    props: ['lista']
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables';

.outer{
    background-color: $bg-footer-black;
    padding: $section-padding;
    position: relative;
}
h2{
    position: absolute;
    top: -22px;
    left: 12.5%;
    display: inline-block;
    padding: 10px 20px;
    background-color: $blue;
    color: white;
    text-transform: uppercase;
    font-size: $advertising-size;
}
.wrapper{
    @include wrapper;
    @include flex-row-between;
    align-items: flex-start;
    row-gap: 50px;
    flex-wrap: wrap;
}
.card{
    @include flex-col-between;
    gap: 20px;
    width: calc(100% / 6);
    padding: 10px;
    border-radius: 5px;
    cursor: pointer;
    position: relative;
    img{
        width: 150px;
        height: 150px;
        object-fit: cover;
        object-position: top;
    }
    div{
        width: 150px;
        color: white;
        font-size: $card-font;
        text-transform: uppercase;
    }
    .price{
        position: absolute;
        right: 20px;
        top: 20px;
        background: #262424;
        width: 40px;
        height: 40px;
        line-height: 40px;
        border-radius: 50%;
        text-align: center;
        opacity: 0;
        transition: all 0.3s;
    }
    &:hover{
        background-color: #262424;
        .price{
            opacity: 0.9;
        }
    }
}
</style>