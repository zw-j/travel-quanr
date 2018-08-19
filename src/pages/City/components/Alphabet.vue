<template>
  <ul class="alphabet">
    <li class="item">A</li>
    <li class="item">A</li>
    <li class="item">A</li>
    <li class="item">A</li>
    <li class="item">A</li>
    <li class="item">A</li>
    <li class="item">A</li>
    <li class="item">A</li>
    <li class="item">A</li>
    <li class="item">A</li>
  </ul>
</template>
<script>
export default {
  name: 'CityAlphabet'
}
</script>
<style lang="stylus" scoped>
  @import "~style/variblee.styl"
  .alphabet
    display flex
    flex-direction column
    justify-content center
    position absolute
    right 0
    bottom 0
    top 1.65rem
    /*background #cacaca*/
    width .35rem
    .item
      text-align center
      line-height:.4rem
      color $bgColor
</style>
