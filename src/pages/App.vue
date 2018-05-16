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

<style lang="scss" rel="stylesheet/scss">

/* Predefine
--------------------- */
$font-stack: sans-serif;

$color-txt-dft: #202020;
$color-txt-red: #dd3915;
$color-bkg-def: #202020;
$color-bkg-red: #dd3915;
$color-bkg-green: #84cf6d;

$header-ht: 70px;
$page-paddaing: 40px;

/* Normal */
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
}

/* Btn */
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

/* Header placeholder */
.hd-placeholder {
  height: $header-ht;
}

</style>
