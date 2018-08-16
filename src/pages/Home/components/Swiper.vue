<template>
  <swiper :options="swiperOption">
    <swiper-slide>
      <img src="~style/image/xh1.jpg" alt="">
    </swiper-slide>
    <swiper-slide>
      <img src="~style/image/xh2.jpg" alt="">
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {}
    }
  }
}
</script>

<style lang="stylus" scoped>
  img
    width:100%;
    height:2.5rem;
</style>
