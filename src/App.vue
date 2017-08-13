<template lang='pug'>

#app
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

</style>