<template>
  <ul class="alphabet">
    <li class="item" v-for="(item,key) of cities" :key="key">{{key}}</li>
  </ul>
</template>
<script>
export default {
  name: 'CityAlphabet',
  props: {
    cities: {
      type: Object
    }
  }
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
