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

html, body, ul, li {
  margin: 0;
  padding: 0;
}

a {
  text-decoration: none;
  color: $color-black-dft;
  cursor: pointer;
}

li {
  list-style: none;
}

// Btn
.btn {
  box-sizing: border-box;
  display: inline-block;
  padding: 13px 25px;
  border: none;
  background-color: $color-black-dft;
  color: $color-white-dft;
  vertical-align: middle;
  font-family: $font-stack;
  cursor: pointer;
  // transition: .1s;
}

.btn-txt {
  @extend .btn;
  padding: 0 3px;
  background-color: transparent;
  color: $color-black-dft;

  &:hover {
    background-color: $color-black-dft;
    color: $color-white-dft;
  }
}

// Header placeholder
.hd-placeholder {
  height: $header-ht;
}

// Arrow
.arrow-right {
  position: absolute;
  top: 50%;
  right: 0;
  display: inline-block;
  width: 8px;
  height: 8px;
  border-top: 1px solid $color-grey-lht;
  border-right: 1px solid $color-grey-lht;
  vertical-align: middle;
  transform: rotate(45deg) translate(-50%);
}

</style>
