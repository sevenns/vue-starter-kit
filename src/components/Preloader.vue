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
  display: flex
  align-items: center
  justify-content: center
  position: fixed
  top: 0
  left: 0
  width: 100%
  height: 100%
  background-color: #FFF

.preloader-fade-enter-active, .preloader-fade-leave-active
  transition: opacity .5s ease, transform .5s ease

.preloader-fade-enter, .preloader-fade-leave-to
  opacity: 0
  transform: scale(1.2)

</style>