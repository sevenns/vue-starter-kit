<template lang='pug'>

.hello
  h1 {{ msg }}

</template>



<script>

export default {
  name: 'hello',
  data () {
    return {
      msg: 'Vue.js starter kit'
    }
  }
}

</script>



<style lang='sass'>

@import ../sass/common/variables
@import ../sass/common/mixins
  
.hello h1
  @include font(light)

</style>