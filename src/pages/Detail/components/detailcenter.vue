<template>
  <div>
    <div class="detail-info">
      <div class="detail-up">
        <div class="up-left">
          <div class="left-com">
            <span class="sore">4.9</span>
            <span class="sore1">分</span>
            <span class="sore2">很棒</span>
          </div>
          <div class="left-command">
            <span class="command1">10314条评论</span>
            <span class="command2">10条攻略</span>
          </div>
          <div class="left-icon">
            <span class="iconfont">&#xe62d;</span>
          </div>
        </div>
        <div class="up-right">
          <div class="right-tro">
            <span>景点简介</span>
          </div>
          <div class="right-time">
            <span>开放时间、贴士</span>
            <span class="iconfont right-icon">&#xe62d;</span>
          </div>
        </div>
      </div>
      <div class="detail-down">
        <span class="iconfont down-icon">&#xe65c;</span>
        <p>海南省三亚市三亚湾西岛</p>
        <span class="iconfont down-right-icon">&#xe62d;</span>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'DetailCenter'
}
</script>
<style lang="stylus" scoped>
  .iconfont
    font-size: .24rem;
  .detail-info
    height 1.98rem
    width 100%
    background white
    .detail-up
      overflow hidden
      height 1.12rem
      border-bottom 1px solid #eee
      .up-left
        width 50%
        float left
        margin-top .24rem
        margin-left .2rem
        .left-icon
          position relative
          top -.5rem
          left 3.05rem
          opacity .5
        .left-com
          color #ff8300;
          .sore
            font-size:.44rem
          .sore1
            margin-left -.08rem
          .sore2
            margin-left .08rem
        .left-command
          font-size .24rem;
          color: #9e9e9e;
          margin-top .1rem
          .command2
            margin-left .08rem
      .up-right
        float left
        margin-top .34rem
        margin-left -.1rem
        .right-tro
          padding-left: .3rem;
          margin-bottom .14rem
        .right-time
          color: #9e9e9e;
          font-size: .24rem;
          padding-left: .3rem;
          .right-icon
            position relative
            top -.22rem
            right -1.2rem
    .detail-down
      overflow hidden
      line-height 100%
      margin-top .3rem
      margin-left .2rem
      p
        float left
      .down-icon
        float left
        display: block;
        color: #9e9e9e;
        font-size: .36rem;
        margin-right .2rem
      .down-right-icon
        float right
        margin-right .15rem
        opacity .5
</style>
