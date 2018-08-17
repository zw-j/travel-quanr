<template>
  <div class="swper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of imgList" :key="item.id">
        <img :src="item.imgUrl" class="swipe-img">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
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
      imgList: [
        {id: '001', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1807/e7/d70d0830a9941b02.jpg_750x200_f8c7d2ad.jpg'},
        {id: '002', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/5e/514ce60160e62602.jpg_750x200_9b0074e2.jpg'},
        {id: '003', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/66/55bc874f100c2d02.jpg_750x200_ac7c05d2.jpg'},
        {id: '004', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/8f/d09fa241a01ac02.jpg_750x200_e0c86013.jpg'}
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .swper >>> .swiper-pagination-bullet-active
    background:#fff;
  .swper
    overflow:hidden
    width:100%;
    height:0;
    padding-bottom:26.7%;
    .swipe-img
      width:100%;
</style>
