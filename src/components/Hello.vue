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

@import '../sass/common/variables'
@import '../sass/common/mixins'


.hello
  h1
    @include font(light)

.hello__content
  align-items: center
  display: flex
  justify-content: center
  min-height: 100vh

.hello__footer
  bottom: 16px
  display: flex
  font-size: rem(18px)
  font-weight: 300
  justify-content: center
  letter-spacing: 2px
  position: absolute
  width: 100%

  a
    color: $grey
    text-decoration: none
</style>
