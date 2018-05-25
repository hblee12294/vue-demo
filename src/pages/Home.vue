<template>
  <main>
    <div class="main-panel">
      <div class="left-panel">
        <cat-navigation></cat-navigation>
      </div>
      <div class="middle-panel">
        <head-slider></head-slider>
        <rising-recipes></rising-recipes>
        <pop-recipes></pop-recipes>
        <questions-block></questions-block>
        <pop-ingredients></pop-ingredients>
      </div>
      <pop-events></pop-events>
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
import PopRecipes from '@/components/Home/PopRecipes'
import QuestionsBlock from '@/components/Home/QuestionsBlock'
import PopIngredients from '@/components/Home/PopIngredients'
import PopEvents from '@/components/Home/PopEvents'

export default {
  name: 'Home',
  components: {
    CatNavigation,
    HeadSlider,
    UserInfo,
    RisingRecipes,
    PopRecipes,
    QuestionsBlock,
    PopIngredients,
    PopEvents
  }
}
</script>

<style lang="scss" scoped>
main {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  padding: 30px $page-pad 0;

  .main-panel {
    flex: 0 0 0%;
    display: flex;
    flex-wrap: wrap;

    .left-panel {
      flex: 0 0 0%;
      padding-right: 40px;
    }

    .middle-panel {
      flex: 0 0 0%;
    }
  }

  .right-panel {
    padding-left: 20px;
  }
}

</style>
