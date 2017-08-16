<template lang='pug'>

.preloader
  vue-loading(type='bubbles', color='#35495E', :size='{ width: "72px", height: "72px"}')

</template>



<script>

import vueLoading from 'vue-loading-template'

export default {
  name: 'preloader',
  components: { vueLoading }
}

</script>



<style lang='sass' scoped>

.preloader
  align-items: center
  background-color: #fff
  display: flex
  height: 100%
  justify-content: center
  left: 0
  position: fixed
  top: 0
  width: 100%
  z-index: 99999

.preloader-fade-enter-active, .preloader-fade-leave-active
  transition: opacity .5s ease, transform .5s ease

.preloader-fade-enter, .preloader-fade-leave-to
  opacity: 0
  transform: scale(1.2)

</style>
