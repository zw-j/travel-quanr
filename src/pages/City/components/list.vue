<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
        <div class="title ">当前城市</div>
        <div class="cur_list">
          <div class="cur_city">
            <div class="cur_btn">
              北京
            </div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title ">热门城市</div>
        <div class="cur_list">
          <div class="cur_city">
            <div class="cur_btn">
              北京
            </div>
          </div>
          <div class="cur_city">
            <div class="cur_btn">
              北京
            </div>
          </div>
          <div class="cur_city">
            <div class="cur_btn">
              北京
            </div>
          </div>
          <div class="cur_city">
            <div class="cur_btn">
              北京
            </div>
          </div>
          <div class="cur_city">
            <div class="cur_btn">
              北京
            </div>
          </div>
          <div class="cur_city">
            <div class="cur_btn">
              北京
            </div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title ">A</div>
        <div class="hot_city_list">
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
        </div>
        <div class="title ">A</div>
        <div class="hot_city_list">
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
        </div>
        <div class="title ">A</div>
        <div class="hot_city_list">
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
        </div>
        <div class="title ">A</div>
        <div class="hot_city_list">
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
        </div><div class="title ">A</div>
        <div class="hot_city_list">
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
          <div class="item">阿拉尔</div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import BScroll from 'better-scroll'
export default {
  name: 'CityList',
  mounted () {
    this.scroll = new BScroll(this.$refs.wrapper)
  }
}
</script>
<style lang="stylus" scoped>
  .list
    background white
    position absolute
    top 1.65rem
    overflow hidden
    left 0
    right 0
    bottom 0
    .title
      line-height .6rem
      background #f4f4f4
      padding-left .2rem
      font-size .26rem
      color #666
      border-bottom 1px solid #d1d1d1
    .cur_list
      padding .1rem .6rem .1rem .1rem
      overflow hidden
    .cur_city
      float:left
      width 33.3%
      .cur_btn
        padding .1rem 0
        margin .1rem
        border:1px solid #c1c1c1
        text-align center
    .hot_city_list
      line-height .6rem
      .item
        border-bottom 1px solid #c9c9c9
        padding-left .2rem
        font-size 13px
</style>
