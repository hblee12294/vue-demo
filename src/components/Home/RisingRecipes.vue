<template>
<div class="rising-recipes">
  <div class="title-bar">
    <div class="title-group">
      <h3 class="title">新秀菜谱</h3>
      <a class="btn-txt" href="">全部</a>
    </div>
    <div class="slider-control">
      <button class="btn" :class="{ disabled: isFirstSlide }" @click="slide(-1)"><i class="arrow-left"></i></button>
      <button class="btn" :class="{ disabled: isLastSlide }" @click="slide(1)"><i class="arrow-right"></i></button>
    </div>
  </div>
  <div class="rising-slider">
    <transition-group tag="ul" class="rising-slides" name="slide">
      <li class="rising-slide" v-for="(slide, index) in slides" :key="index" v-show="index === currentIndex">
        <div class="recipe-single" v-for="(recipe, index) in slide" :key="index">
          <a class="recipe-img" href="" target="_blank">
            <img :src="recipe.src" :alt="recipe.title">
          </a>
          <div class="recipe-title">
            <a href="" target="_blank" :title="recipe.title">{{ recipe.title }}</a>
          </div>
        </div>
      </li>
    </transition-group>
  </div>
</div>
</template>

<script>
export default {
  name: 'RisingRecipes',
  data () {
    return {
      currentIndex: 0,
      recipes: [{
        title: '酥皮月饼-芝麻桂花馅（附视频菜谱）',
        src: 'http://s1.cdn.xiachufang.com/ff3e02628bad11e6a9a10242ac110002_4030w_2688h.jpg@2o_50sh_1pr_1l_150w_90h_1c_1e_90q_1wh',
        href: ''
      }, {
        title: '红糖麦芬',
        src: 'http://s1.cdn.xiachufang.com/94e81dd6885f11e6b87c0242ac110003_4912w_2760h.jpg@2o_50sh_1pr_1l_150w_90h_1c_1e_90q_1wh',
        href: ''
      }, {
        title: '减脂南瓜藜麦饭',
        src: 'http://s2.cdn.xiachufang.com/21b1e95a45f14ae789e4afd61d0c15fa_5472w_3648h.jpg?imageView2/1/w/150/h/90/interlace/1/q/90',
        href: ''
      }, {
        title: '奶酪陷阱里的三角饭团',
        src: 'http://s2.cdn.xiachufang.com/b4e52f548a5b11e6a9a10242ac110002_6000w_4000h.jpg?imageView2/1/w/150/h/90/interlace/1/q/90',
        href: ''
      }, {
        title: '眉豆花生鸡脚汤',
        src: 'http://s2.cdn.xiachufang.com/22a7b1ac8ae211e6b87c0242ac110003_1080w_1440h.jpg?imageView2/1/w/150/h/90/interlace/1/q/90',
        href: ''
      }, {
        title: '紫薯溶豆',
        src: 'http://s2.cdn.xiachufang.com/9fbc852aa9704bf5ae409d0e9bd79cfe_480w_384h.jpg?imageView2/1/w/150/h/90/interlace/1/q/90',
        href: ''
      }, {
        title: '盆栽冰激凌',
        src: 'http://s2.cdn.xiachufang.com/f930e89a885f11e6a9a10242ac110002_640w_960h.jpg?imageView2/1/w/150/h/90/interlace/1/q/90',
        href: ''
      }, {
        title: '布朗尼（好时巧克力酱）',
        src: 'http://s1.cdn.xiachufang.com/2f8c874ba64d4c52b218a9e923e00fb6_3264w_2448h.jpg@2o_50sh_1pr_1l_150w_90h_1c_1e_90q_1wh',
        href: ''
      }, {
        title: '白菜丸子粉丝汤',
        src: 'http://s2.cdn.xiachufang.com/aff7d03089e511e6b87c0242ac110003_2047w_1493h.jpg?imageView2/1/w/150/h/90/interlace/1/q/90',
        href: ''
      }, {
        title: '篮球球衣蛋糕',
        src: 'http://s1.cdn.xiachufang.com/e5238116688611e7947d0242ac110002_3500w_2334h.jpg@2o_50sh_1pr_1l_150w_90h_1c_1e_90q_1wh',
        href: ''
      }, {
        title: '各种口味的柠檬司康',
        src: 'http://s1.cdn.xiachufang.com/1913bb676e7b40f1806ee4dfb7e55ab0_1808w_1279h.jpg@2o_50sh_1pr_1l_150w_90h_1c_1e_90q_1wh',
        href: ''
      }, {
        title: '茄子烧五花肉',
        src: 'http://s1.cdn.xiachufang.com/f2dfe89a888e11e6a9a10242ac110002_640w_480h.jpg@2o_50sh_1pr_1l_150w_90h_1c_1e_90q_1wh',
        href: ''
      }, {
        title: '软软小面包',
        src: 'http://s1.cdn.xiachufang.com/b4f0dcc2898011e6b87c0242ac110003_1248w_834h.jpg@2o_50sh_1pr_1l_150w_90h_1c_1e_90q_1wh',
        href: ''
      }, {
        title: '豆浆杂粮粥',
        src: 'http://s1.cdn.xiachufang.com/bb229792d4c8439e8ecc505f3d2b8394_3739w_2671h.jpg@2o_50sh_1pr_1l_150w_90h_1c_1e_90q_1wh',
        href: ''
      }, {
        title: '上汤豆苗（超级快手菜）',
        src: 'http://s2.cdn.xiachufang.com/1939ba0016d011e7947d0242ac110002_1280w_960h.jpg?imageView2/1/w/150/h/90/interlace/1/q/90',
        href: ''
      }]
    }
  },
  computed: {
    slides () {
      let arr = []
      let start = 0
      let recipes = this.recipes

      while (start + 3 < recipes.length) {
        arr.push(recipes.slice(start, start + 3))
        start += 3
      }

      return arr
    },
    isFirstSlide () {
      return this.currentIndex === 0
    },
    isLastSlide () {
      return this.currentIndex === this.slides.length - 1
    }
  },
  methods: {
    slide (step) {
      const nextIndex = this.currentIndex + step

      if (nextIndex >= 0 && nextIndex < this.slides.length) {
        this.currentIndex = nextIndex
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.rising-recipes {
  display: inline-block;
  width: 490px;

  .title-bar {
    display: flex;
    justify-content: space-between;

    .title-group {
      display: flex;
      align-items: center;

      .title {
        margin: 15px 0;
        color: $color-gold-dft;
        font-size: $font-sz-lg;
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

    .slider-control {
      display: flex;
      align-items: center;

      .btn {
        position: relative;
        height: 27px;
        width: 27px;
        padding: 0;
        margin: 2px;
        outline: none;
        background-color: $color-grey-lhter;

        &:hover {
          background-color: $color-grey-lht;
        }
      }

      .disabled {
        cursor: auto;

        i {
          border-color: $color-grey-dsabl;
        }

        &:hover {
          background-color: $color-grey-lhter;
        }
      }

      .arrow-left {
        left: 25%;
        border-color: $color-grey-dft;
      }

      .arrow-right {
        right: 25%;
        border-color: $color-grey-dft;
      }
    }
  }
}

.rising-slider {
  position: relative;
  overflow: hidden;
  height: 130px;

  .rising-slides {
    .rising-slide {
      position: absolute;
      display: flex;
      justify-content: space-between;
      min-width: 490px;
    }

    .recipe-single {
      width: 150px;

      .recipe-title {
        padding: 8px 4px;
        overflow: hidden;
        white-space: nowrap;
        text-align: center;
        text-overflow: ellipsis;

        a:hover {
          color: $color-red-dft;
        }
      }
    }
  }
}

.slide-enter-active {
  transition: all .5s ease;
  transform: translateX(0);
}
.slide-leave-active {
  transition: all .5s ease;
  transform: translateX(-100%);
}
.slide-enter {
  transform: translateX(100%);
}
.slide-leave {
  transform: translateX(0);
}

</style>
