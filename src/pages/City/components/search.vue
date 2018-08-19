<template>
  <div class="search">
    <input type="text" class="input-search" placeholder="输入城市名或拼音">
  </div>
</template>
<script>
export default {
  name: 'CitySearch'
}
</script>
<style lang="stylus" scoped>
  @import '~style/variblee.styl'
  .search
    line-height .72rem;
    padding .1rem
    background $bgColor
    .input-search
      margin-top -.3rem
      box-sizing border-box
      width: 100%
      line-height .65rem
      text-align center
      border-radius .06rem
      border:none
      padding 0 .1rem
      color: gray
    .input-search::-webkit-input-placeholder
      color #ccc
</style>
