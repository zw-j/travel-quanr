<template>
  <div class="container" @click="handleClose">
    <div class="warp">
      <swiper :options="swiperOptions">
        <swiper-slide v-for="(item,index) in images" :key= "index">
          <img class="gallery-img" :src="item">
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>
<script>
export default {
  name: 'CommonGallery',
  props: {
    images: {
      type: Array,
      default () {
        return []
      }
    }
  },
  methods: {
    handleClose () {
      this.$emit('Close')
    }
  },
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        paginationType: 'fraction',
        observeParents: true,
        observer: true
      }
    }
  }
}
</script>
<style lang="stylus" scoped>
  .container >>> .swiper-container
    overflow inherit
  .container
    display: flex
    z-index: 99
    position absolute
    top 0
    bottom 0
    left 0
    right 0
    flex-direction column
    justify-content center
    background black
    .warp
      width 100%
      height 257.14px
      .gallery-img
        width 100%
    .swiper-pagination
      color #fff
      position absolute
      bottom -2rem
</style>
