<template>
  <div class="headline">
    <div class="head-slider">
      <transition-group tag="ul" class="head-slides" name="slide">
        <li class="head-slide" v-for="(slide, index) in slides" :key="index" v-show="index===currentIndex"  @mouseover="stopSlide" @mouseout="startSlide">
          <a class="head-link" href="" target="_blank">
            <img :src="slide.src" :alt="slide.title">
          </a>
          <div class="head-info">
            <a class="head-title">{{ slide.title }}</a>
            <div class="head-footnote">
              <a class="head-num">{{ slide.num }} 人做过这道菜</a><a class="head-author" :href="slide.author.href">by {{ slide.author.name }}</a>
            </div>
          </div>
        </li>
      </transition-group>
    </div>
    <div class="indicator">
      <ul class="dots">
        <li class="dot" v-for="(slide, index) in slides" :key="index" @click="slideTo(index)" :class="{'active': index === currentIndex}"></li>
      </ul>
      <a class="head-history" href="">
        <span></span><span></span><span></span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderSlider',
  data () {
    return {
      currentIndex: 0,
      interval: 2500,
      slides: [{
        title: '肉炒杏鲍菇',
        src: 'http://s2.cdn.xiachufang.com/6551618c87b411e6a9a10242ac110002_1600w_899h.jpg?imageView2/1/w/490/h/260/interlace/1/q/90',
        href: '/recipe/1094345/',
        num: 813,
        author: {
          name: '胶P糖',
          href: '/cook/10438907/'
        }
      }, {
        title: '黑糖珍珠鲜奶-在家喝鹿角巷',
        src: 'http://s1.cdn.xiachufang.com/445a7834a57e45b4b97ead7705e4b43c_3232w_2424h.jpg@2o_50sh_1pr_1l_490w_260h_1c_1e_90q_1wh',
        href: '/recipe/103008748/',
        num: 91,
        author: {
          name: '黄花',
          href: '/cook/10022624/'
        }
      }, {
        title: '日式汉堡肉 附最快手百搭日式红酒酱汁',
        src: 'http://s2.cdn.xiachufang.com/1733f58ed6fc47a88c896ed06713e6a3_5225w_7833h.jpg?imageView2/1/w/490/h/260/interlace/1/q/90',
        href: '/recipe/102755051/',
        num: 10,
        author: {
          name: 'CherCerf鹿儿',
          href: '/cook/103367524/'
        }
      }, {
        title: 'LADY M 抹茶千层可丽饼/千层蛋糕 Green Tea Mille Crepes',
        src: 'http://s2.cdn.xiachufang.com/047fc448883111e6a9a10242ac110002_600w_600h.jpg?imageView2/1/w/490/h/260/interlace/1/q/90',
        href: '/recipe/100136819/',
        num: 3566,
        author: {
          name: 'Kuma爱的果酱',
          href: '/cook/101462238/'
        }
      }, {
        title: 'Q弹饱满的香辣小龙虾',
        src: 'http://s2.cdn.xiachufang.com/5a94c0c28b2e11e6b87c0242ac110003_620w_380h.jpg?imageView2/1/w/490/h/260/interlace/1/q/90',
        href: '/recipe/101834397/',
        num: 237,
        author: {
          name: '橘丽丝',
          href: '/cook/103996281/'
        }
      }]
    }
  },
  computed: {
    prevSlide () {
      if (this.currentIndex === 0) {
        return this.slides.length - 1
      } else {
        return this.currentIndex - 1
      }
    },
    nextSlide () {
      if (this.currentIndex === this.slides.length - 1) {
        return 0
      } else {
        return this.currentIndex + 1
      }
    }
  },
  methods: {
    slideTo (index) {
      this.currentIndex = index
      this.stopSlide()
      this.startSlide()
    },
    startSlide () {
      this.intId = setInterval(() => {
        this.slideTo(this.nextSlide)
      }, this.interval)
    },
    stopSlide () {
      clearInterval(this.intId)
    }
  },
  mounted () {
    this.startSlide()
  }
}
</script>

<style lang="scss" scoped>
.headline {
  display: inline-block;
  vertical-align: top;
  height: 280px;
  text-align: center;

  .indicator {
    display: inline-block;

    .dots {
      display: inline-block;

      .dot {
        box-sizing: border-box;
        display: inline-block;
        height: 7px;
        width: 7px;
        margin: 0 2px;
        border: 1px solid $color-grey-dft;
        border-radius: 50%;
        cursor: pointer;
      }

      .active {
        background-color: $color-grey-dft;
      }
    }

    .head-history {
      display: inline-block;
      vertical-align: middle;
      width: 16px;
      margin-left: 3px;
      margin-right: -50%;
      font-size: 0;
      text-align: left;

      span {
        display: inline-block;
        height: 2px;
        width: 15px;
        margin: 1px 0;
        background-color: $color-grey-dft;

        &:last-child {
          width: 12px;
        }
      }
    }
  }
}

.head-slider {
  position: relative;
  overflow: hidden;
  min-height: 260px;
  min-width: 490px;
  background-color: $color-black-dft;

  .head-slide {
    position: absolute; // Why slide items must be absolute

    img {
      opacity: .7;
    }

    .head-info {
      position: absolute;
      bottom: 0;
      left: 0;
      padding: 20px;
      pointer-events: none;

      a {
        color: $color-white-dft;
        font-size: $font-sz-sm;
      }

      .head-title {
        display: inline-block;
        margin-bottom: 5px;
        font-size: $font-sz-lger;
        font-weight: bold;
      }

      .head-author {
        margin-left: 10px;
        pointer-events: auto;
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
