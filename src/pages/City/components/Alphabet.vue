<template>
  <ul class="alphabet">
    <li class="item" v-for="item of letters" :key="item"
        :ref="item"
        @click="handleClick" @touchstart="handleTouchStart"
        @touchend="handleTouchEnd"
        @touchmove="handleTouchMove"
    >{{item}}</li>
  </ul>
</template>
<script>
export default {
  data () {
    return {
      touchStatus: false
    }
  },
  name: 'CityAlphabet',
  computed: {
    letters () {
      const letter = []
      for (let i in this.cities) {
        letter.push(i)
      }
      return letter
    }
  },
  props: {
    cities: {
      type: Object
    }
  },
  methods: {
    handleClick (e) {
      this.$emit('change', e.target.innerText)
    },
    handleTouchStart () {
      this.touchStatus = true
    },
    handleTouchMove (e) {
      if (this.touchStatus) {
        const StartY = this.$refs['A'][0].offsetTop
        const TouchY = e.touches[0].clientY - 79
        const index = Math.floor((TouchY - StartY) / 20)
        if (index >= 0 && index < this.letters.length) {
          this.$emit('change', this.letters[index])
        }
      }
    },
    handleTouchEnd () {
      this.touchStatus = false
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import "~style/variblee.styl"
  .alphabet
    display flex
    flex-direction column
    justify-content center
    position absolute
    right 0
    bottom 0
    top 1.65rem
    /*background #cacaca*/
    width .35rem
    .item
      text-align center
      line-height:.4rem
      color $bgColor
</style>
