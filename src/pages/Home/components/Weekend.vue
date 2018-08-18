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
    line-height 25px;
    padding-top 5px;
    a
      margin-right 20px;
  .footer
    height 1.4rem
    background #eeeeee
    border-bottom 1.5px solid  #d5d5d5
    .down_list
      list-style none
      width 300px;
      margin 0 auto
      line-height 39px;
      li
        float:left
        width 60px;
        height:39px
        margin-right 10px;
    .up_list
      overflow hidden
      list-style none
      line-height 40px;
      width 320px;
      margin 0 auto
      a
        color:gray
      div
        float: left;
        width: 22px;
        height: 22px;
        background: url("~style/image/nav_7.png") 0 0 no-repeat;
        background-size: 175px 50px;
        margin-top 10px;
        margin-right 3px;
      .hotel
        div
          background-position: -25px 0;
      .house
        div
          background-position: -150px 0px;
      li
        float:left
        width 75px;
        height 31px;
  .all
    background white
    line-height .6rem
    text-align center
    font-size 12px
    position relative
    .span-icon
      position absolute
      left 5px;
      top -1px
    .span_info
      margin-left -15px
      .span_price
        font-size 13px;
  .info
    list-style none
    width:375px;
    height:202.39px;
    background white;
    border-bottom 2.5px solid #d5d5d5
    .info-img-wrap
      width 100%;
      .info-img
        width 375px;
        height 139.08px;
    .info-text
      padding-top .2rem
      padding-left .2rem
      .text-title
        font-size 14px;
      .text-content
        font-size 13px
        margin-top .18rem
</style>
