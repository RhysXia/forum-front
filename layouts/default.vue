<template lang='pug'>
  div.layout
    Header
    nuxt
    Footer
</template>
<script>
import Header from '@/components/layout/header'
import Footer from '@/components/layout/footer'
export default {
  components: {
    Header,
    Footer
  }
}
</script>
<style lang="scss" scoped>
.layout{
}
</style>

