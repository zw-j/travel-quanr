<template>
  <div>
    <div class="header_item" v-show="header_item">
      <span class="post_door">门票</span>
      <span class="one_day">一日游</span>
      <span class="hap_item">娱乐项目</span>
    </div>
    <div class="header_item header_show" v-show="!header_item">
      <span class="post_door" :class="{bottom_bor:active}">门票</span>
      <span class="one_day">一日游</span>
      <span class="hap_item">娱乐项目</span>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HeaderItem',
  data () {
    return {
      header_item: true,
      active: false
    }
  },
  methods: {
    handleHeaderScroll () {
      const scrollTop = document.documentElement.scrollTop
      if (scrollTop > 540) {
        this.header_item = false
        this.active = true
      } else {
        this.header_item = true
      }
    }
  },
  mounted () {
    window.addEventListener('scroll', this.handleHeaderScroll)
  }
}
</script>
<style lang="stylus" scoped>
  /*.bottom_bor*/
    /*border-bottom 2px solid #13a1d6*/
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
    z-index:3
    position fixed
    top .7rem
    left 0
    right  0
</style>
