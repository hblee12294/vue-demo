<template>
  <div id="app">
    <header>
      <div class="hd-item logo">
        <img src="@/assets/logo.png" alt="logo">
      </div>
      <div class="hd-item search">
        <input
          class="ipt-search"
          placeholder="搜索菜谱、食材"
          v-model="searchText"><button class="btn clr-bg">搜菜谱</button>
      </div>
      <div class="hd-item menu">
        <button class="btn-txt clr-txt">会员专区</button>
        <button class="btn-txt clr-txt">菜谱分类</button>
        <button class="btn-txt clr-txt">菜单</button>
        <button class="btn-txt clr-txt">作品动态</button>
      </div>
      <div class="hd-item login">
        <button class="btn-txt clr-txt">登陆</button>
        <button class="btn-txt clr-txt">注册</button>
      </div>
    </header>
    <!-- <router-view/> -->
    <app-footer></app-footer>
  </div>
</template>

<script>
import AppFooter from '@/components/AppFooter'
export default {
  name: 'App',
  components: {
    AppFooter
  },
  data () {
    return {
      searchText: ''
    }
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

/* Header
--------------------- */
header {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  height: 70px;
}

.ipt-search {
  box-sizing: border-box;
  width: 300px;
  height: 44px;
  padding: 8px;
  outline: none;
  border: 1px solid #f3f3f3;
  color: #222222;
  font-size: 16px;
  letter-spacing: 1px;
  vertical-align: middle;
  transition: .2s;
}

.ipt-search:focus {
  border: 1px solid #909090;
}

.search .btn {
  height: 44px;
  padding: 0px 16px;
  font-size: 16px;
}

.menu .btn-txt {
  font-size: 16px;
}

.login .btn-txt {
  font-size: 16px;
}

</style>
