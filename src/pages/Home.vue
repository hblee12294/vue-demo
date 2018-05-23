<template>
  <main>
    <div class="left-panel">
      <cat-navigation></cat-navigation>
    </div>
    <div class="middle-panel">
      <head-slider></head-slider>
      <rising-recipes></rising-recipes>
    </div>
    <div class="right-panel">
      <user-info></user-info>
    </div>
  </main>
</template>

<script>
import CatNavigation from '@/components/Home/CatNavigation'
import HeadSlider from '@/components/Home/HeadSlider'
import UserInfo from '@/components/Home/UserInfo'
import RisingRecipes from '@/components/Home/RisingRecipes'

export default {
  name: 'Home',
  components: {
    CatNavigation,
    HeadSlider,
    UserInfo,
    RisingRecipes
  }
}
</script>

<style lang="scss" scoped>
main {
  display: flex;
  padding: 30px $page-pad 0;

  .left-panel {
    padding-right: 40px;
  }

  .right-panel {
    padding-left: 20px;
  }
}

</style>
