<template>
  <div>
    <div class="header_item">
      <span class="post_door">门票</span>
      <span class="one_day">一日游</span>
      <span class="hap_item">娱乐项目</span>
    </div>
    <div class="header_item header_show">
      <span class="post_door">门票</span>
      <span class="one_day">一日游</span>
      <span class="hap_item">娱乐项目</span>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HeaderItem',
  methods: {
    handleHeaderScroll () {
      const scrolled = document.documentElement.scrollTop
      console.log(scrolled)
    }
  },
  activated () {
    window.addEventListener('scroll', this.handleHeaderScroll)
  }
}
</script>
<style lang="stylus" scoped>
  .header_item
    line-height .5rem
    background white
    padding .2rem .8rem
    font-size .32rem
    margin-top .15rem
    border-bottom 1px solid #ccc
    .one_day
      margin-left 1.51rem
    .hap_item
      margin-left 1.19rem
  .header_show
    position fixed
    top .62rem
    left 0
    right  0
</style>
