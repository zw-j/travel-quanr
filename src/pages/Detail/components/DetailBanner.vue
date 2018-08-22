<template>
  <div>
    <div class="banner" @click="handleImgClick">
      <img :src="bannerImg"
           class="banner-img">
      <div class="banner-info">
        <div class="info_con">
          {{sightName}}
        </div>
        <div class="info-number">
          <span class="iconfont">&#xe633;</span>
          <span>{{this.gallaryImgs.length}}</span>
        </div>
      </div>
    </div>
    <detail-fade>
     <common-gallery :images="gallaryImgs" v-show="flag" @Close="handleClose"></common-gallery>
    </detail-fade>
  </div>
</template>
<script>
import CommonGallery from 'common/gallery/Gallery'
import DetailFade from 'common/fade-ainmation/fade'
export default {
  props: {
    sightName: String,
    bannerImg: String,
    gallaryImgs: Array
  },
  data () {
    return {
      flag: false
    }
  },
  name: 'DetailBanner',
  components: {
    CommonGallery,
    DetailFade
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
