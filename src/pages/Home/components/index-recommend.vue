<template>
  <div>
    <div class="title">热门推荐</div>
    <ul class="info-list">
      <li class="info" v-for="item of recommendList" :key="item.id">
        <div class="info-img-wrap">
          <a href="#"><img class="info-img" :src="item.imgUrl"></a>
        </div>
        <div class="info-text">
          <p class="text-title">{{item.title}}</p>
          <p class="text-content">{{item.content}}</p>
          <a href="#"><button>查看详情</button></a>
        </div>
      </li>
    </ul>
    <div class="all">查看所有产品</div>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    recommendList: {
      type: Array
    }
  }
}
</script>

<style lang="stylus" scoped>
.title
  line-height .7rem;
  background #ccc;
  text-indent 1em;
.all
  background white
  line-height .8rem
  text-align center
  color: #00afc7
.info
  list-style none
  width:7.5rem;
  height:2rem;
  background white;
  border-bottom .01rem solid #d5d5d5
  .info-img-wrap
    float left;
    padding:.1rem
    .info-img
      width 1.8rem;
      height 1.8rem;
  .info-text
    float:left;
    padding-top .2rem
    .text-title
      font-weight bold
      font-size .32rem;
    .text-content
      color #bbbbbb
      margin-top .18rem
    button
      margin-top .23rem
      color white
      background orangered
      border none
      border-radius .03rem;
      padding-left .2rem
      padding-right .2rem
      font-weight bold
</style>
