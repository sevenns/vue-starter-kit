<template lang='pug'>

.hello
  transition(name='preloader-fade')
    preloader(v-if='loading')
  h1 {{ msg }}

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
  
.hello h1
  @include font(light)

</style>