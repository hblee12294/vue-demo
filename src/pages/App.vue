<template>
  <div id="app">
    <app-header></app-header>
    <!-- <router-view/> -->
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

<style>
/* Predefine
------------------- */
#app {
  color: #202020;
  font-family: sans-serif;
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
  background-color: #797979;
  color: white;
  vertical-align: middle;
  cursor: pointer;
}

.btn-txt {
  border: none;
  background-color: transparent;
  cursor: pointer;
}

.clr-txt {
  color: #dd3915;
}

.clr-bg {
  background-color: #dd3915;
}

.clr-bg-2 {
  background-color: #84cf6d;
}

</style>
