<template>
  <div>
    <div class="item">
      <div class="item-title" v-for="(item,index) of list" :key="index">
        <div class="item-info">
          <span class="item-icon"></span>
          {{item.title}}
        </div>
        <div v-if="item.children" class="item-children">
          <detail-list :list="item.children"></detail-list>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    list: {
      type: Array
    }
  },
  name: 'DetailList'
}
</script>
<style lang="stylus" scoped>
  .item-title
    line-height .8rem
    font-size .32rem
    .item-info
      padding-left .2rem
      border-bottom 1px solid #ccc
      .item-icon
        display: inline-block;
        position: relative;
        top .06rem
        left .06rem
        width: .36rem;
        height: .36rem;
        background: url(http://s.qunarzz.com/piao/image/touch/sight/detail.png) 0 -.45rem no-repeat;
        background-size: .4rem 3rem;
    .item-children
      padding-left .4rem
</style>
