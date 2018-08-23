<template>
  <div>
    <div class="title">周末哪里</div>
    <ul class="info-list">
      <li class="info" v-for="item of weekendList" :key="item.id">
        <div class="info-img-wrap">
          <a href="#"><img class="info-img" :src="item.imgUrl"></a>
        </div>
        <div class="info-text">
          <p class="text-title">{{item.title}}</p>
          <p class="text-content">{{item.content}}</p>
        </div>
      </li>
    </ul>
    <div class="all">
        <span class="span-icon">①</span>
        <div class="span_info">
          <span class="span_price">票面价</span>
          是指通过景区指定窗口售卖的纸质门票上标注的价格
        </div>
    </div>
    <div class="footer">
      <div class="footer_up">
        <ul class="up_list">
          <li class="plane">
            <a href="#">
              <div></div>
              <span>机票</span>
            </a>
          </li>
          <li class="hotel">
            <a href="#">
              <div></div>
              <span>酒店</span>
            </a>
          </li>
          <li class="house">
            <a href="#">
              <div></div>
              <span>公寓</span>
            </a>
          </li>
          <li class="more">
            <a href="#">
              <div></div>
              <span>更多</span>
            </a>
          </li>
        </ul>
      </div>
      <div class="footer_down">
        <ul class="down_list">
          <li><a href="#">登录</a></li>
          <li><a href="#">我的订单</a></li>
          <li><a href="#">最近浏览</a></li>
          <li><a href="#">关于我们</a></li>
        </ul>
      </div>
    </div>
    <div class="footer_nav">
      <div class="foo_nav_up">
        <a href="#">触屏版</a>
        <a href="#">电脑版</a>
      </div>
      <div class="foo_nav_down">
        <p>
          Qunar 京ICP备05021087意见反馈
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    weekendList: {
      type: Array
    }
  }
}
</script>

<style lang="stylus" scoped>
  .title
    line-height .7rem;
    background #efefef;
    text-indent 1em;
  .footer_nav
    height 1.2rem
    background #eeeeee
    text-align center
    line-height .5rem;
    padding-top .05rem;
    a
      margin-right .4rem;
  .footer
    height 1.4rem
    background #eeeeee
    border-bottom .015rem solid  #d5d5d5
    .down_list
      list-style none
      width 6rem;
      margin 0 auto
      line-height .78rem;
      li
        float:left
        width 1.2rem;
        height:.78rem
        margin-right .1rem;
    .up_list
      overflow hidden
      list-style none
      line-height .8rem;
      width 6.4rem;
      margin 0 auto
      a
        color:gray
      div
        float: left;
        width: .44rem;
        height: .44rem;
        background: url(http://source.qunarzz.com/site/images/wap/touch/images/v2/images2x/nav_7.png) 0 0 no-repeat;
        background-size: 3.5rem 1rem;
        margin-top .1rem;
        margin-right .03rem;
      .hotel
        div
          background-position: -.5rem 0;
      .house
        div
          background-position: -3rem 0;
      li
        float:left
        width 1.5rem;
        height .62rem;
  .all
    background white
    line-height .6rem
    text-align center
    font-size .24rem
    position relative
    .span-icon
      position absolute
      left .05rem;
      top -.01rem
    .span_info
      margin-left -.3rem
      .span_price
        font-size .26rem;
  .info
    list-style none
    width:7.5rem;
    height:4.05rem;
    background white;
    border-bottom .025rem solid #d5d5d5
    .info-img-wrap
      width 100%;
      .info-img
        width 7.5rem;
        height 2.78rem;
    .info-text
      padding-top .2rem
      padding-left .2rem
      .text-title
        font-size .28rem;
      .text-content
        font-size .26rem
        margin-top .18rem
</style>
