<template>
  <div>
    <div class="banner" @click="handleImgClick">
      <img src="http://img1.qunarzz.com/sight/p0/1412/85/fc4b88c4d559fd35dfc0f66e0f0e2ee5.water.jpg_350x240_54ff894e.jpg"
           class="banner-img">
      <div class="banner-info">
        <div class="info_con">
          西岛(AAAA景区)
        </div>
        <div class="info-number">
          <span class="iconfont">&#xe633;</span>
          <span>27</span>
        </div>
      </div>
    </div>
    <common-gallery :images="images" v-show="flag" @Close="handleClose"></common-gallery>
  </div>
</template>
<script>
import CommonGallery from 'common/gallery/Gallery'
export default {
  data () {
    return {
      flag: false,
      images: [
        'http://img1.qunarzz.com/sight/p0/1412/85/fc4b88c4d559fd35dfc0f66e0f0e2ee5.water.jpg_350x240_54ff894e.jpg',
        'http://img1.qunarzz.com/sight/p0/1412/85/fc4b88c4d559fd35dfc0f66e0f0e2ee5.water.jpg_350x240_54ff894e.jpg'
      ]
    }
  },
  name: 'DetailBanner',
  components: {
    CommonGallery
  },
  methods: {
    handleImgClick () {
      this.flag = true
    },
    handleClose () {
      this.flag = false
    }
  }
}
</script>
<style lang="stylus" scoped>
  .banner
    overflow hidden
    position relative
    .banner-img
      width 100%
      height 206.25px
    .banner-info
      position absolute
      bottom 0
      left 0
      right 0
      color white
      margin-bottom .1rem
      padding 0 .2rem
      background-image linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,.8))
      .info-number
        float right
        height .3rem
        border-radius .4rem
        text-align center
        padding .08rem .2rem
        background rgba(255,255,255,.1.2);
      .info_con
        font-size .32rem
        float left
        margin-top .1 rem
</style>
