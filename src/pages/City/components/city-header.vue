<template>
  <div class="header">
    <router-link to="/">
      <span class="iconfont city-icon">&#xe605;</span>
    </router-link>
    城市选择
  </div>
</template>
<script>
export default {
  name: 'CityHeader'
}
</script>
<style lang="stylus" scoped>
  @import "~style/variblee.styl"
  .header
    line-height .86rem
    background $bgColor
    text-align center
    color #fff
    position relative
    .city-icon
      position absolute
      top:0;
      left .15rem
      color #fff
</style>
