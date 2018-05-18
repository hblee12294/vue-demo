<template>
  <main>
    <category-nav></category-nav>
  </main>
</template>

<script>
import CategoryNav from '@/components/Home/CategoryNav'

export default {
  name: 'Home',
  components: {
    CategoryNav
  }
}
</script>

<style lang="scss" scoped>
main {
  display: flex;
  padding: 30px $page-pad 0;
}

</style>
