<template lang='pug'>

#app
  icon(name='vue', color='#42b983 #35495E', width="256", height="256")
  router-view

</template>



<script>

import './components/icons'

export default {
  name: 'app'
}

</script>



<style lang='sass'>

// Plugins
@import ../node_modules/sanitize.css/sanitize

// Common
@import ./sass/common/fonts
@import ./sass/common/mixins
@import ./sass/common/variables

// Base
@import ./sass/primary/_base

#app
  display: flex
  flex-direction: row
  align-items: center
  justify-content: center
  height: 100vh

</style>