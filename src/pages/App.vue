<template>
  <div id="app">
    <app-header></app-header>
    <div class="hd-placeholder"></div>
    <router-view/>
    <app-footer></app-footer>
  </div>
</template>

<script>
import AppHeader from '@/components/AppHeader'
import AppFooter from '@/components/AppFooter'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppFooter
  }
}
</script>

<style lang="scss">

// Normal
#app {
  font-family: $font-stack;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

html, body {
  margin: 0;
  padding: 0;
}

a {
  text-decoration: none;
  color: $color-txt-dft;
}

// Btn
.btn {
  box-sizing: border-box;
  padding: 13px 25px;
  border: none;
  background-color: $color-bkg-def;
  color: white;
  vertical-align: middle;
  cursor: pointer;
}

.btn-txt {
  @extend .btn;
  padding: 0 3px;
  background-color: transparent;
  color: $color-txt-dft;
}

// Header placeholder
.hd-placeholder {
  height: $header-ht;
}

</style>
