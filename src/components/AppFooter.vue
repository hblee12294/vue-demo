<template>
  <footer>
      <div class="ft-item coop">
        <button class="btn clr-bg-2">入驻下厨房市集</button>
        <button class="btn clr-bg-2">广告合作</button>
      </div>
      <div class="ft-item info">
        <div class="sitemap">
          <a href="">美食生活杂志</a>
          <a href="">厨房工作</a>
          <a href="">帮助中心</a>
          <a href="">联系我们</a>
          <a href="">意见反馈</a>
          <a href="">隐私声明</a>
        </div>
        <div class="copyright">
          <div>Copyright © iachufang.com 京B2-20180499 <a href="http://www.miibeian.gov.cn">京ICP备13009078号-1</a> 京公网安备11010802022310号</div>
          <div>违法和不良信息举报电话：13581683297 举报邮箱：talk@xiachufang.com</div>
        </div>
      </div>
      <div class="ft-item social">
        <div class="scl-icons">
          <a href="https://weibo.com/xiachufang" target="_blank"><img src="@/assets/sinaweibo.svg" title="微博" alt="微博"></a>
          <a href="https://twitter.com/xiachufang" target="_blank"><img src="@/assets/twitter.svg" title="推特" alt="推特"></a>
        </div>
        <div class="slogan">唯有美食与爱不可辜负</div>
      </div>
    </footer>
</template>

<script>
export default {
  name: 'AppFooter'
}
</script>

<style>
footer {
  display: flex;
  flex-wrap: wrap;
  padding: 10px 40px;
  color: #909090;
  font-size: 13px;
}

/* Cooperation */
.coop {
  padding: 15px 0;
  flex: 0 0 100%;
}

.coop .btn {
  margin-right: 20px;
  font-size: 13px;
}

/* Information */
.info {
  flex: auto;
}

.info a {
  color: #909090;
}

.info div {
  padding: 3px 0;
}

/* Copyright */
.copyright div {
  padding: 3px 0;
}

/* Social Media */
.social {
  flex: auto;
  text-align: right;
}

.scl-icons img {
 height: 18px;
 margin-left: 5px;
}

.social div {
  padding: 3px 0;
}

</style>
