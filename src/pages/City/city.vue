<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
    <city-list :hot="hot" :cities="cities" :letter="letter"></city-list>
    <city-alphabet :cities="cities" @change="handleLetter"></city-alphabet>
  </div>
</template>
<script>
import axios from 'axios'
import CityHeader from './components/city-header'
import CitySearch from './components/search'
import CityList from './components/list'
import CityAlphabet from './components/Alphabet'

export default {
  data () {
    return {
      cities: {},
      hot: [],
      letter: ''
    }
  },
  name: 'City',
  mounted () {
    this.getCityInfo()
  },
  methods: {
    getCityInfo () {
      axios.get('/api/city.json')
        .then(this.getCityList)
    },
    getCityList (res) {
      const xhr = res.data
      if (xhr.ret && xhr) {
        this.hot = xhr.data.hotCities
        // console.log(this.hot)
        this.cities = xhr.data.cities
        // console.log(this.cities)
        // console.log(res)
      }
    },
    handleLetter (letter) {
      this.letter = letter
    }
  },
  components: {
    CityHeader,
    CitySearch,
    CityList,
    CityAlphabet
  }
}
</script>
<style lang="stylus" scoped>
</style>
