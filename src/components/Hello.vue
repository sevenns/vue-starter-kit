<template lang='pug'>

.hello
  transition(name='preloader-fade')
    preloader(v-if='loading')

  .hello__content
    icon(name='vue', color='#42b983 #35495E', width="256", height="256")
    h1 {{ msg }}

  .hello__footer
    a(href='http://sevenns.com/', target='_blank') alexander sevenns

</template>



<script>

import preloader from './Preloader'

export default {
  name: 'hello',
  components: { preloader },
  data () {
    return {
      msg: 'Vue.js starter kit',
      loading: true
    }
  },
  mounted () {
    setTimeout(() => {
      this.loading = false
    }, 500)
  }
}

</script>



<style lang='sass'>

@import ../sass/common/variables
@import ../sass/common/mixins

.hello__content
  display: flex
  align-items: center
  justify-content: center
  min-height: 100vh

.hello__footer
  position: absolute
  bottom: 16px
  width: 100%
  display: flex
  justify-content: center
  font-weight: 300
  letter-spacing: 2px
  font-size: rem(18px)

  a
    text-decoration: none
    color: #35495E

.hello h1
  @include font(light)

</style>