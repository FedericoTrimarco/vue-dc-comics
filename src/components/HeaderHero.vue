<template>
    <div class="hero">
        <div class="hero-bg">
            <div class="container-two">
                <span>CURRENT SERIES</span>
            </div>
        </div>
        <div class="hero-products">
            <div class="container-two">
                <ul class="list-style-none d-flex flex-wrap">
                    <li v-for="(card, index) in products" :key="`card-${index}`">
                        <CardProps :url="card.thumb" :title="card.series"/>
                    </li>
                </ul>
            </div>
        </div>
        <div class="load text-center">
            <span>Load More</span>
        </div>
    </div>
</template>

<script>
import Card from '@/data/Card.js';
import CardProps from '@/components/CardsProps.vue';
export default {
    name: 'HeaderHero',
    components:{
        CardProps,
    },
    data(){
        return{
            products: Card,
        }
    }
}
</script>

<style scoped lang="scss">
@import '@/styles/generals';
@import '@/styles/variables';
@import '@/styles/utilities';
.hero{
    background-color: #1c1c1c;
    color: #fff;
    padding-bottom: 30px;
}
.hero-bg{
    height: 550px;
    background-image: url('../assets/jumbotron.jpg');
    background-size: cover;

    .container-two{
        position: relative;
        height: 100%;
        span{
            font-size: 30px;
            font-weight: bold;
            padding: 20px;
            background-color: $color_primary;
            position: absolute;
            top: 93%;
            left: 0;
        }
    }
    
}

.hero-products{
    
    color: white;
    padding: 100px 0;

    li{
        width: calc(100% / 6);
        padding: 20px;
        margin-bottom: 10px;

    }
}
.load{
    span{
        color: white;
        padding: 10px 50px;
        font-size: 20px;
        font-weight: bold;
        background-color: $color_primary;

    }
}

</style>