<template>
  <header>
    <div class="hd-item logo">
      <img src="@/assets/logo.png" alt="logo">
    </div>
    <div class="hd-item search">
      <input
        class="ipt-search"
        placeholder="搜索菜谱、食材"
        v-model="searchText"><button class="btn">搜菜谱</button>
    </div>
    <div class="hd-item menu">
      <button class="btn-txt">会员专区</button>
      <button class="btn-txt">菜谱分类</button>
      <button class="btn-txt">菜单</button>
      <button class="btn-txt">作品动态</button>
    </div>
    <div class="hd-item login">
      <button class="btn-txt">登陆</button>
      <button class="btn-txt">注册</button>
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

<style lang="scss" scoped>
header {
  position: fixed;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  height: $header-ht;
  width: 100%;
  background-color: white;
  border-bottom: $border;
  box-shadow: 0 2px 2px -2px rgba(0, 0, 0, .08);
}

.search {
  .ipt-search {
    box-sizing: border-box;
    width: 300px;
    height: 44px;
    padding: 8px;
    outline: none;
    border: $border;
    color: $color-txt-dft;
    font-size: $font-sz-dft;
    letter-spacing: 1px;
    vertical-align: middle;
    transition: .2s;
    &:focus {
      border: 1px solid #909090;
    }
  }
  .btn {
    height: 44px;
    padding: 0px 16px;
    background-color: $color-bkg-red;
    font-size: $font-sz-dft;
  }
}

.menu {
  .btn-txt {
    color: $color-txt-red;
    font-size: $font-sz-dft;
  }
}

.login {
 .btn-txt {
    color: $color-txt-red;
    font-size: $font-sz-dft;
  }
}

</style>
