<template>
  <div class="pop-ings">
    <div class="title-bar">
      <div class="title-group">
        <h3 class="title">时令食材</h3>
        <a class="btn-txt" href="">全部</a>
      </div>
    </div>
      <ul class="ingredients">
        <li class="ingredient" v-for="(ingredient, index) in ingredients" :key="index">
          <a href="">
            <img :src="ingredient.src" :alt="ingredient.name">
            <span>{{ ingredient.name }}</span>
          </a>
        </li>
      </ul>
  </div>
</template>

<script>
export default {
  name: 'PopIngredients',
  data () {
    return {
      ingredients: [{
        name: '小龙虾',
        src: 'http://s2.cdn.xiachufang.com/5921e6f87c9211e59786e35152605765.jpg?imageView2/1/w/60/h/60/interlace/1/q/90',
        href: '/category/5322/'
      }, {
        name: '独蒜',
        src: 'http://s2.cdn.xiachufang.com/a17d9514243146f89835d3ecdfedfe03_220w_192h.jpg?imageView2/1/w/60/h/60/interlace/1/q/90',
        href: '/category/5201/'
      }, {
        name: '鸡爪',
        src: 'http://s1.cdn.xiachufang.com/1949c26b7c9211e5988845d1d992f1cb.jpg@2o_50sh_1pr_1l_60w_60h_1c_1e_90q_1wh',
        href: '/category/1337/'
      }, {
        name: '百香果',
        src: 'http://s2.cdn.xiachufang.com/16fcd4e87c9211e58a0f9dc38687f4d3.jpg?imageView2/1/w/60/h/60/interlace/1/q/90',
        href: '/category/1246/'
      }, {
        name: '笋',
        src: 'http://s2.cdn.xiachufang.com/fa83bcde7c9111e5afe4a9bfb5aebcdb.jpg?imageView2/1/w/60/h/60/interlace/1/q/90',
        href: '/category/534/'
      }, {
        name: '紫洋葱',
        src: 'http://s2.cdn.xiachufang.com/a51e773fce8a453e9bf9a77ae66b6bde_450w_300h.jpg?imageView2/1/w/60/h/60/interlace/1/q/90',
        href: '/category/5313/'
      }, {
        name: '春笋',
        src: 'http://s2.cdn.xiachufang.com/15ae11427c9211e5aaa89dc38687f4d3.jpg?imageView2/1/w/60/h/60/interlace/1/q/90',
        href: '/category/1224/'
      }, {
        name: '河虾',
        src: 'http://s2.cdn.xiachufang.com/e6ea98287c9111e5876545d1d992f1cb.jpg?imageView2/1/w/60/h/60/interlace/1/q/90',
        href: '/category/76/'
      }, {
        name: '柠檬',
        src: 'http://s2.cdn.xiachufang.com/1886910c7c9211e5855245d1d992f1cb.jpg?imageView2/1/w/60/h/60/interlace/1/q/90',
        href: '/category/1299/'
      }, {
        name: '龙虾',
        src: 'http://s1.cdn.xiachufang.com/37e9f7787c9211e5b66ab82a72e00100.jpg@2o_50sh_1pr_1l_60w_60h_1c_1e_90q_1wh',
        href: '/category/2918/'
      }, {
        name: '蒜苔',
        src: 'http://s2.cdn.xiachufang.com/71207d25151943cebefda563c8dd83b6_300w_206h.jpg?imageView2/1/w/60/h/60/interlace/1/q/90',
        href: '/category/1003510/'
      }, {
        name: '芦笋',
        src: 'http://s2.cdn.xiachufang.com/f3dbf13a7c9111e5922bb82a72e00100.jpg?imageView2/1/w/60/h/60/interlace/1/q/90',
        href: '/category/364/'
      }]
    }
  }
}
</script>

<style lang="scss" scoped>
.pop-ings {
  display: inline-block;
  width: 490px;

  .title-bar {
    display: flex;
    justify-content: space-between;
    align-items: center;

    .title-group {
      display: flex;
      align-items: center;

      .title {
        margin: 15px 0;
        color: $color-gold-dft;
        font-size: $font-sz-lg;
      }
    }

    .btn-txt {
      margin-left: 15px;
      color: $color-red-dft;
      font-size: $font-sz-md;

      &:hover {
        background-color: $color-red-dft;
        color: $color-white-dft;
      }
    }
  }
}

.ingredients {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  padding: 15px 15px 7px;
  background-color: $color-grey-lhter;

  .ingredient {
    width: 60px;
    margin: 0 4px 13px;
    text-align: center;

    &:hover {
      img {
        opacity: .9;
      }

      span {
        color: $color-red-dft;
      }
    }

    span {
      margin-top: 4px;
      font-size: $font-sz-smer;
    }
  }
}

</style>
