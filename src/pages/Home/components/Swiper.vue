<template>
  <div class="swper">
    <swiper :options="swiperOption" v-if="swiperList.length">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img :src="item.imgUrl" class="swipe-img">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  props: {
    swiperList: {
      type: Array
    }
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 1500,
        speed: 800
      }
    }
  },
  mounted () {
    setTimeout(() => {
      this.autoplay = !this.autoplay
    }, 4000)
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
