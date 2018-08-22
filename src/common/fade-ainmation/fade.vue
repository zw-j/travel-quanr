<template>
  <transition>
    <slot></slot>
  </transition>
</template>
<script>
export default {
  name: 'DetailFade'
}
</script>
<style lang="stylus" scoped>
  .v-enter,.v-leave-to
    opacity: 0;
  .v-leave-active,.v-enter-active
    transition .8s opacity
</style>
