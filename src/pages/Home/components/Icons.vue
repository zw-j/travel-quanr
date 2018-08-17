<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icons-item" v-for="item of page" :key="item.id">
          <a href="#">
            <img :src="item.imgUrl">
            <p>{{item.name}}</p>
          </a>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination'
        // direction: 'left'
      },
      imgList: [
        {
          id: '001',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          name: '景点门票'
        },
        {
          id: '002',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
          name: '北京必游'
        },
        {
          id: '003',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6a/45f595250c73d102.png',
          name: '夏日玩水'
        },
        {
          id: '004',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
          name: '文化古迹'
        },
        {
          id: '005',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
          name: '动植物园'
        },
        {
          id: '006',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
          name: '故宫'
        },
        {
          id: '007',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
          name: '一日游'
        },
        {
          id: '008',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/95/8d02011d149bdb02.png',
          name: '汽车票'
        },
        {
          id: '009',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
          name: '故宫'
        }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.imgList.forEach((key, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(key)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~style/minins.styl"
  .icons >>> .swiper-container
    width:100%;
    height 185.7px;
    background:white;
  .icons-item
    width:93.75px;
    height:80px;
    float:left;
    text-align center
    margin-top 10px;
    /*background #25a4bb*/
   .icons-item:nth-of-type(5),
   .icons-item:nth-of-type(6),
   .icons-item:nth-of-type(7),
   .icons-item:nth-of-type(8)
     margin-top -3px;
    a
      color:black;
      padding-bottom 5px;
      p
        line-height 25px;
        ellipsis();
    img
      width:55px;
      height:55px;
</style>
