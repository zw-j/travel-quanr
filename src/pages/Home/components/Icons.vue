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
    height 3.714rem;
    background:white;
  .icons-item
    width:1.875rem;
    height:1.6rem;
    float:left;
    text-align center
    margin-top .2rem;
    /*background #25a4bb*/
   .icons-item:nth-of-type(5),
   .icons-item:nth-of-type(6),
   .icons-item:nth-of-type(7),
   .icons-item:nth-of-type(8)
     margin-top -.06rem;
    a
      color:black;
      padding-bottom .1rem;
      p
        line-height .5rem;
        ellipsis();
    img
      width:1.1rem;
      height:1.1rem;
</style>
