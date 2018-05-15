<template>
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
</template>

<script>
export default {
  name: 'AppHeader',
  data () {
    return {
      searchText: ''
    }
  }
}
</script>

<style>
header {
  position: fixed;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  height: 70px;
  width: 100%;
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
