<template>
  <div class="header">
    <div class="header_left">
      <span class="iconfont">&#xe605;</span>
    </div>
    <div class="header_input">
      <span class="iconfont">&#xe632;</span>
        输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header_right">
        {{this.$store.state.city}}
        <span class="iconfont icon-city">&#xe6aa;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>
<style lang="stylus" scoped>
  @import '~style/variblee.styl'
  .header
    display flex;
    line-height :.86rem;
    background :$bgColor
    color:#fff;
    .header_input
      flex:1
      background :#ffffff;
      color:#cccc;
      border-radius:.1rem;
      height:.62rem;
      margin-top:.12rem;
      margin-left:.2rem;
      line-height:.62rem;
      font-size:.3rem;
      padding-left:.05rem
    .header_left
      width:.64rem;
      float:left;
      text-align center;
    .header_right
      min-width:1.24rem
      padding-left .1rem
      float:right;
      text-align:center;
      font-size:.3rem;
      color:#fff
      .icon-city
        font-size:.40rem;
        margin-left:-.05rem;
</style>
