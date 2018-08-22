<template>
  <div>
    <detail-banner :sightName="sightName" :bannerImg="bannerImg"
    :gallaryImgs="gallaryImgs"></detail-banner>
    <detail-header></detail-header>
    <div class="content">
      <detail-center></detail-center>
      <detail-list :list="categoryList"></detail-list>
    </div>
  </div>
</template>

<script>
import DetailBanner from './components/DetailBanner'
import DetailHeader from './components/detaiilheader'
import DetailList from './components/detail-list'
import DetailCenter from './components/detailcenter'
import axios from 'axios'

export default {
  data () {
    return {
      sightName: '',
      bannerImg: '',
      gallaryImgs: [],
      categoryList: []
    }
  },
  methods: {
    getDetailInfo () {
      axios.get('api/detail.json', {
        params: {
          id: this.$route.params.id
        }
      }).then(this.getDetailData)
    },
    getDetailData (xhr) {
      const currentData = xhr.data
      if (currentData.ret && currentData.data) {
        const data = currentData.data
        this.sightName = data.sightName
        this.bannerImg = data.bannerImg
        this.gallaryImgs = data.gallaryImgs
        this.categoryList = data.categoryList
      }
    }
  },
  mounted () {
    this.getDetailInfo()
  },
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList,
    DetailCenter
  }
}
</script>

<style lang="stylus" scoped>
  .content
    height:50rem
</style>
