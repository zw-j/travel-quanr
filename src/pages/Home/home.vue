<template>
  <div class="home">
    <home-header></home-header>
    <home-swiper :swiperList="swiperList"></home-swiper>
    <home-icons :iconsList="iconsList"></home-icons>
    <home-recommend :recommendList="recommendList"></home-recommend>
    <home-weekend :weekendList="weekendList"></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/index-recommend'
import HomeWeekend from './components/Weekend'
import axios from 'axios'
import { mapState } from 'vuex'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  data () {
    return {
      swiperList: [],
      iconsList: [],
      recommendList: [],
      weekendList: [],
      lastCity: ''
    }
  },
  computed: {
    ...mapState(['city'])
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json?city=' + this.city)
        .then(this.getHomeSucc)
    },
    getHomeSucc (xhr) {
      const data = xhr.data
      const dataList = data.data
      if (data.ret && dataList) {
        this.swiperList = dataList.swiperList
        this.iconsList = dataList.iconsList
        this.recommendList = dataList.recommendList
        this.weekendList = dataList.weekendList
      }
    }
  },
  mounted () {
    this.getHomeInfo()
    this.lastCity = this.city
  },
  activated () {
    if (this.city !== this.lastCity) {
      this.lastCity = this.city
      this.getHomeInfo()
    }
  }
}
</script>
<style>

</style>
