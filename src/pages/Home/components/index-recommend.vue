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
    <div class="all">查看所有产品</div>
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
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1507/2b/61926c532a022890e52ae233e093792c.water.jpg_200x200_6d5ebe13.jpg',
          title: '惠州平安峡漂流',
          content: '从所未有的刺激漂流体验'
        },
        {
          id: '003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1605/c7/c7dd06252f0ff0af90.water.jpg_200x200_95cb2c7d.jpg',
          title: '惠州平安峡漂流',
          content: '从所未有的刺激漂流体验'
        },
        {
          id: '005',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/ae/ae40b952c637b458.water.jpg_200x200_9606b7bc.jpg',
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
.all
  background white
  line-height .8rem
  text-align center
  color: #00afc7
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
