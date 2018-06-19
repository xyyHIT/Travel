<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
            <!-- slides -->
            <swiper-slide v-for="item of swiperList" :key="item.id"><img :src=item.imgUrl class="img-swiper"></swiper-slide>
            <!-- Optional controls -->
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>

</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '1',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1707/90/2ab6fd356529aa02.jpg_750x200_4120afc5.jpg'
      }, {
        id: '2',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/56/d939255eab633a02.jpg_750x200_c08a2c07.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active
        background: #fff
    .wrapper
        overflow hidden
        width 100%
        height 0
        padding-bottom 31.25%
        background #eee
        .img-swiper
            width 100%
</style>
