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
  props: {
    iconsList: {
      type: Array
    }
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination'
        // direction: 'left'
      }
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconsList.forEach((key, index) => {
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
