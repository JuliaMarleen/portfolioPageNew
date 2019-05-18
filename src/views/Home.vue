<template>
  <div class="home">
    <!-- <business-card/> -->
    <!-- <background-lines/> -->
    <text-box/>
  </div>
</template>

<script>
// @ is an alias to /src
// import BusinessCard from '@/components/BusinessCard.vue'
// import BackgroundLines from '@/components/BackgroundLines.vue'
import TextBox from '@/components/TextBox.vue'

export default {
  name: 'home',
  components: {
    // BusinessCard,
    // BackgroundLines,
    TextBox
  }
}
</script>

<style lang="scss" scoped>
</style>
