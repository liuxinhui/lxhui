<template>
    <div class="swiper">
        <swiper :options="swiperOption">
            <swiper-slide><img class="swiper-img" src="https://imgs.qunarzz.com/vc/28/72/3d/07df240399f309da18e9a9854e.png_92.png" /></swiper-slide>
            <swiper-slide><img class="swiper-img" src="https://imgs.qunarzz.com/vc/42/26/bb/71d41bf5d04fcb589ece936cba.jpg_92.jpg" /></swiper-slide>
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
    name:'HomeSwiper',
    data (){
        return{
            swiperOption:{
                pagination:'swiper-pagination',
                loop: true
            }
        }
    }
}
</script>

<style lang="stylus" scoped>
    .swiper
        width :100%
        height :0
        overflow :hidden
        padding-bottom :40%
        .swiper-img
            width :100%
</style>