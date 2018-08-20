<template>
  <div>
    <div class="search">
      <input type="text" v-model="keyword" class="input-search"
             placeholder="输入城市名或拼音">
    </div>
    <div class="search-content" ref="search_flag" v-show="this.keyword">
      <ul>
        <li class="search-item" @click="handleCityClick(item.name)"
            v-for="item of list" :key="item.id">{{item.name}}</li>
        <li class="search-item" v-show="!this.list.length">没有找到匹配地点</li>
      </ul>
    </div>
    </div>
</template>
<script>
import Bscroll from 'better-scroll'
export default {
  data () {
    return {
      keyword: '',
      list: [],
      timer: null,
      flag: true
    }
  },
  mounted () {
    this.BScroll = new Bscroll(this.$refs.search_flag)
  },
  methods: {
    handleCityClick (city) {
      this.$store.commit('changeCity', city)
      this.$router.push('/')
    }
  },
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      if (!this.keyword) {
        this.list = []
        return
      }
      this.timer = setTimeout(() => {
        const result = []
        for (let i in this.cities) {
          this.cities[i].forEach((value) => {
            if (value.spell.indexOf(this.keyword) > -1 ||
                value.name.indexOf(this.keyword) > -1) {
              result.push(value)
            }
          })
        }
        this.list = result
      }, 100)
    }
  },
  props: {
    cities: {
      type: Object
    }
  },
  name: 'CitySearch'
}
</script>
<style lang="stylus" scoped>
  @import '~style/variblee.styl'
  .search
    line-height .72rem;
    padding .1rem
    background $bgColor
    .input-search
      margin-top -.3rem
      box-sizing border-box
      width: 100%
      line-height .65rem
      text-align center
      border-radius .06rem
      border:none
      padding 0 .1rem
      color: gray
    .input-search::-webkit-input-placeholder
      color #ccc
  .search-content
    z-index 1
    overflow hidden
    position:absolute
    top 1.65rem
    bottom 0;
    left 0
    right 0
    background white
    .search-item
      line-height .62rem
      border-bottom .01rem solid #ccc
      padding-left .2rem
</style>
