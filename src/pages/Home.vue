<template>
  <main>
    <cat-navigation></cat-navigation>
    <head-slider></head-slider>
    <!-- <head-slider></head-slider> -->
    <!-- <head-slider></head-slider> -->
  </main>
</template>

<script>
import CatNavigation from '@/components/Home/CatNavigation'
import HeadSlider from '@/components/Home/HeadSlider'

export default {
  name: 'Home',
  components: {
    CatNavigation,
    HeadSlider
  }
}
</script>

<style lang="scss" scoped>
main {
  padding: 30px $page-pad 0;
}

</style>
