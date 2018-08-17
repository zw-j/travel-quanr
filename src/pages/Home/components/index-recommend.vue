<template>
  <div>
    <div class="title">热门推荐</div>
    <ul class="info-list">
      <li class="info" v-for="item of contentList" :key="item.id">
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
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      contentList: [
        {
          id: '001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1704/a4/a4511cb08f87f662a3.water.jpg_200x200_3b639896.jpg',
          title: '惠州平安峡漂流',
          content: '从所未有的刺激漂流体验'
        },
        {
          id: '002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1704/a4/a4511cb08f87f662a3.water.jpg_200x200_3b639896.jpg',
          title: '惠州平安峡漂流',
          content: '从所未有的刺激漂流体验'
        },
        {
          id: '003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1704/a4/a4511cb08f87f662a3.water.jpg_200x200_3b639896.jpg',
          title: '惠州平安峡漂流',
          content: '从所未有的刺激漂流体验'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.title
  line-height .7rem;
  background #ccc;
  text-indent 1em;
.info
  list-style none
  width:375px;
  height:100px;
  background white;
  border-bottom 1px solid #d5d5d5
  .info-img-wrap
    float left;
    padding:.1rem
    .info-img
      width 90px;
      height 90px;
  .info-text
    float:left;
    padding-top .2rem
    .text-title
      font-weight bold
      font-size 16px;
    .text-content
      color #bbbbbb
      margin-top .18rem
    button
      margin-top .23rem
      color white
      background orangered
      border none
      border-radius 3px;
      padding-left .2rem
      padding-right .2rem
      font-weight bold
</style>
