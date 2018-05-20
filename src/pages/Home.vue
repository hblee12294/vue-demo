<template>
  <main>
    <cat-navigation></cat-navigation>
    <head-slider></head-slider>
    <user-info></user-info>
  </main>
</template>

<script>
import CatNavigation from '@/components/Home/CatNavigation'
import HeadSlider from '@/components/Home/HeadSlider'
import UserInfo from '@/components/Home/UserInfo'

export default {
  name: 'Home',
  components: {
    CatNavigation,
    HeadSlider,
    UserInfo
  }
}
</script>

<style lang="scss" scoped>
main {
  padding: 30px $page-pad 0;
}

</style>
