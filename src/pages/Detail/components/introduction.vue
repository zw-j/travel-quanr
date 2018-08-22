<template>
  <div class="city_tro">
    <div class="tro_header">
      <span class="tro_icon"></span>
      <span class="tro_tit">去哪儿推荐</span>
    </div>
    <div class="tro_list">
      <div class="item">
        <div class="item_left">
          <h6 class="left_title">【暑期大促】西岛-畅玩精品套票</h6>
          <div>
              <span class="item_con">
                <img class="item_con_img" src="https://img1.qunarzz.com/piao/fusion/1804/f0/39deb48037c83702.png" alt="">
                14:00前可订今日,预订后1小时可用
              </span>
          </div>
          <div class="tro_lab_list">
              <span class="item_lab">
                <img class="item_con_img" src="https://img1.qunarzz.com/piao/fusion/1804/b0/c3cf2897c74ecc02.png" alt="">
                自营
              </span>
            <span class="item_lab">
                随时退
              </span>
          </div>
        </div>
        <div class="item_right">
          <div class="item_price">
            <span class="mon_price">¥</span>
            <span class="price_num">460</span>
          </div>
          <button class="buy_btn">预订</button>
        </div>
      </div>
      <div class="item">
        <div class="item_left">
          <h6 class="left_title">【暑期大促】西岛-畅玩精品套票</h6>
          <div>
              <span class="item_con">
                <img class="item_con_img" src="https://img1.qunarzz.com/piao/fusion/1804/f0/39deb48037c83702.png" alt="">
                14:00前可订今日,预订后1小时可用
              </span>
          </div>
          <div class="tro_lab_list">
              <span class="item_lab">
                <img class="item_con_img" src="https://img1.qunarzz.com/piao/fusion/1804/b0/c3cf2897c74ecc02.png" alt="">
                自营
              </span>
            <span class="item_lab">
                随时退
              </span>
          </div>
        </div>
        <div class="item_right">
          <div class="item_price">
            <span class="mon_price">¥</span>
            <span class="price_num">460</span>
          </div>
          <button class="buy_btn">预订</button>
        </div>
      </div>
      <div class="item">
        <div class="item_left">
          <h6 class="left_title">【暑期大促】西岛-畅玩精品套票</h6>
          <div>
              <span class="item_con">
                <img class="item_con_img" src="https://img1.qunarzz.com/piao/fusion/1804/f0/39deb48037c83702.png" alt="">
                14:00前可订今日,预订后1小时可用
              </span>
          </div>
          <div class="tro_lab_list">
              <span class="item_lab">
                <img class="item_con_img" src="https://img1.qunarzz.com/piao/fusion/1804/b0/c3cf2897c74ecc02.png" alt="">
                自营
              </span>
            <span class="item_lab">
                随时退
              </span>
          </div>
        </div>
        <div class="item_right">
          <div class="item_price">
            <span class="mon_price">¥</span>
            <span class="price_num">460</span>
          </div>
          <button class="buy_btn">预订</button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'DetailIntroduction'
}
</script>
<style lang="stylus" scoped>
  .item_con_img
    display: inline-block;
    width: .2rem;
    max-height: .32rem;
    margin-right: .04rem;
    vertical-align: 0;
  .city_tro
    overflow hidden
    margin-top .18rem
    background white
    .tro_header
      line-height .88rem
      padding-left .2rem
      border-bottom 1px solid #e5e5e5
      .tro_icon
        display: inline-block;
        margin-bottom -.06rem
        width: .36rem;
        height: .36rem;
        background: url(http://s.qunarzz.com/piao/image/touch/sight/detail.png) 0 -.45rem no-repeat;
        background-size: .4rem 3rem;
      .tro_tit
        font-size .3rem
    .item
      overflow hidden
      background white
      width 100%
      padding .3rem .2rem .2rem .2rem
      border-bottom 1px solid #ccc
      .item_left
        float left
        .left_title
          margin-bottom .1rem
        .item_con
          display: inline-block;
          height: .32rem;
          color: #616161;
          font-size: .24rem;
          line-height: .32rem;
          white-space: nowrap;
        .tro_lab_list
          margin-top .05rem
          .item_lab
            padding .01rem
            color #16cbec
            display inline-block
            font-size .1rem
            border 1px solid rgba(37,164,187,.2)
            border-radius .08rem
            background rgba(37,164,187,.05)
      .item_right
        float right
        padding-right .5rem
        .item_price
          color: #ff8a0d;
          font-weight bold
          .mon_price
            font-size: .27rem;
          .price_num
            font-size: .4rem;
            line-height: .4rem;
        .buy_btn
          border none
          border-radius .07rem
          background #ff8a0d
          color white
          font-weight bold
          line-height .58rem
          padding 0 .5rem
    .item:last-child
      border:none
</style>
