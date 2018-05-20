<template>
  <div class="user-info">
    <div class="login">
      <ul class="login-third-party">
        <li><button class="btn"><i class="login-icon"></i>QQ 登陆</button></li>
        <li><button class="btn"><i class="login-icon"></i>微博登陆</button></li>
      </ul>
      <ul class="login-links">
        <li><a href="" class="btn-txt">手机/邮箱登陆</a></li>
        <li><a href="" class="btn-txt">注册</a></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'UserInfo'
}
</script>

<style lang="scss" scoped>
.user-info {
  display: inline-block;
  min-height: 200px;
  min-width: 290px;
  margin-left: 20px; // For testing
  padding: 30px 5px;
  margin-bottom: 30px;
  background-color: $color-grey-lhter;
  text-align: center;
  line-height: 1.2;

  .login {
    padding-top: 30px;

    .login-third-party {
      .btn {
        width: 150px;
        padding: 10px 25px 10px 10px;
        margin-bottom: 5px;
        background-color: $color-red-dft;
        font-size: $font-sz-md;
      }

      .login-icon {
        display: inline-block;
        vertical-align: middle;
        height: 16px;
        width: 16px;
        margin-right: 8px;
        background: none no-repeat 0;
        background-image: url('../../assets/login-icon.png');
      }
    }
  }
}

@for $i from 1 through 2 {
  .login .login-third-party li:nth-child(#{$i}) {
    .login-icon {
      background-position: 0 #{-30 * ($i - 1)}px;
    }
  }
}

</style>
