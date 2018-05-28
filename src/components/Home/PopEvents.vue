<template>
  <div class="pop-events">
    <h3 class="pop-events-head">
      <div class="title">
        参照<span class="num">{{ recipesNum }}</span>菜谱，大家做出<span class="num">{{ dishesNum }}</span>作品
      </div>
      <div class="links">
        <a class="btn-txt" href="">最新上传</a>
        <a class="btn-txt" href="">正在流行</a>
        <a class="btn-txt" href="">24小时最佳</a>
      </div>
    </h3>
    <ul class="events">
      <li class="event" v-for="(event, index) in events" :key="index">
        <a href="">
          <div class="summary">
            <span class="tag">#{{ event.tag }}#</span>
            <span class="description">{{ event.description }}</span>
          </div>
          <div class="posts">
            <img v-for="(post, index) in event.posts" :key="index" :src="post.src" :alt="post.title">
          </div>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'PopEvents',
  data () {
    return {
      recipesNum: 1048259,
      dishesNum: 41063404,
      events: [{
        tag: '今天也要好好吃早餐',
        description: '好好吃一顿早餐',
        posts: [{
          title: '牛奶红茶贝果',
          src: 'http://s2.cdn.xiachufang.com/3cf6f30fde08445ba7065c732f2e868a_1280w_853h.jpg?imageView2/1/w/280/h/280/interlace/1/q/90'
        }, {
          title: '早餐•2017年8月17日',
          src: 'http://s2.cdn.xiachufang.com/5759122808814c4595993eea95154a48_1280w_929h.jpg?imageView2/1/w/280/h/280/interlace/1/q/90'
        }, {
          title: '早餐•2017年6月16日',
          src: 'http://s2.cdn.xiachufang.com/cf448c6c522b11e7bc9d0242ac110002_1280w_1215h.jpg?imageView2/1/w/280/h/280/interlace/1/q/90'
        }]
      }, {
        tag: '我爱的戚风蛋糕，我要把你做到最好',
        description: '最爱戚风蛋糕，对我来说，戚风就是每天吃都喜欢，两天不吃就会想的一种食物～所以一定...',
        posts: [{
          title: '我的戚风蛋糕',
          src: 'http://s1.cdn.xiachufang.com/764bae47f2eb442c908c84e5d3e5aa9d_1616w_1080h.jpg@2o_50sh_1pr_1l_280w_280h_1c_1e_90q_1wh'
        }, {
          title: '私房小技能分享：如何烤出更高的蛋糕胚',
          src: 'http://s2.cdn.xiachufang.com/b0187a5ce7074a3cb5716d88c715d650_988w_741h.jpg?imageView2/1/w/280/h/280/interlace/1/q/90'
        }, {
          title: '我的戚风蛋糕',
          src: 'http://s2.cdn.xiachufang.com/d45e262fbd304293b9d37b817b4fd6cd_992w_744h.jpg?imageView2/1/w/280/h/280/interlace/1/q/90'
        }]
      }, {
        tag: '宿舍小厨房',
        description: '就算条件简陋、食材有限、没有背景、没有道具依然挡不住我们一颗爱做(zhe)饭(teng)的...',
        posts: [{
          title: '午餐•2017年5月4日',
          src: 'http://s1.cdn.xiachufang.com/a9b23eee307111e7947d0242ac110002_1280w_960h.jpg@2o_50sh_1pr_1l_280w_280h_1c_1e_90q_1wh'
        }, {
          title: '午餐•2017年5月4日',
          src: 'http://s2.cdn.xiachufang.com/9331dd3c307111e7bc9d0242ac110002_1280w_960h.jpg?imageView2/1/w/280/h/280/interlace/1/q/90'
        }, {
          title: '早餐马拉松顺利收官：因为坚持，所以更好！',
          src: 'http://s1.cdn.xiachufang.com/1c8f3c5a2f9611e7947d0242ac110002_960w_1280h.jpg@2o_50sh_1pr_1l_280w_280h_1c_1e_90q_1wh'
        }]
      }, {
        tag: '厨神养成计划',
        description: '准高三 开学了也要为了成为一个酷炫的厨神做准备拔草升级中 ︿(￣︶￣)︿',
        posts: [{
          title: '快手炒乌冬',
          src: 'http://s2.cdn.xiachufang.com/3df0a2a2eca34a7b9d055758d33f9ac7_1280w_1280h.jpg?imageView2/1/w/280/h/280/interlace/1/q/90'
        }, {
          title: '简单的紫菜包饭',
          src: 'http://s2.cdn.xiachufang.com/b39c584b75af4074a5481b2bcb5564f7_1280w_1280h.jpg?imageView2/1/w/280/h/280/interlace/1/q/90'
        }, {
          title: '酸甜蔓越莓馒头 -- 谁都会有少女心',
          src: 'http://s1.cdn.xiachufang.com/c7f11d170f6f11e6acc3292115f33bc0.jpg@2o_50sh_1pr_1l_280w_280h_1c_1e_90q_1wh'
        }]
      }, {
        tag: '美滋滋的下午茶',
        description: 'cheat day',
        posts: [{
          title: '午餐•2017年1月18日',
          src: 'http://s2.cdn.xiachufang.com/70470708dd4111e6bc9d0242ac110002_1620w_1620h.jpg?imageView2/1/w/280/h/280/interlace/1/q/90'
        }, {
          title: '周末在厨房 | 晒晒你爱的餐具',
          src: 'http://s2.cdn.xiachufang.com/13faa017f0ed4c2f93eeae198e9d68b3_1215w_1620h.jpg?imageView2/1/w/280/h/280/interlace/1/q/90'
        }, {
          title: '零失败的 ---可可布朗尼',
          src: 'http://s2.cdn.xiachufang.com/6c7d975be709496f8f1a25f6d456dd7d_1213w_1099h.jpg?imageView2/1/w/280/h/280/interlace/1/q/90'
        }]
      }, {
        tag: '24小时流行作品',
        description: '每张照片背后都有故事，几句寒暄传递生活的力量。',
        posts: [{
          title: '早餐•2018年5月25日',
          src: 'http://s2.cdn.xiachufang.com/f89cc8c3d0e747f6abae7b17654df9ba_1279w_1280h.jpg?imageView2/1/w/280/h/280/interlace/1/q/90'
        }, {
          title: '多力 | 为爱做品质三餐',
          src: 'http://s2.cdn.xiachufang.com/16dd2e7fb34546b996ec9fa0404e437d_1600w_2000h.jpg?imageView2/1/w/280/h/280/interlace/1/q/90'
        }, {
          title: '晚餐•2018年5月24日',
          src: 'http://s1.cdn.xiachufang.com/dc97f0976cc34c509f29ca7b7ad37ff2_1280w_1280h.jpg@2o_50sh_1pr_1l_280w_280h_1c_1e_90q_1wh'
        }]
      }]
    }
  }
}
</script>

<style lang="scss" scoped>
.pop-events {
  display: inline-block;
  min-width: 660px;

  .pop-events-head {
    padding: 32px;
    margin-bottom: 2px;
    background-color: $color-grey-lhter;

    .title {
      margin-bottom: 5px;
      color: $color-gold-dft;
      font-size: $font-sz-lgmd;

      .num {
        margin: 0 5px;
        color: $color-red-fade;
      }
    }

    .links {
      .btn-txt {
        margin-right: 32px;
        color: $color-red-dft;
        font-size: $font-sz-md;

        &:hover {
          color: $color-white-dft;
          background-color: $color-red-dft;
        }
      }
    }
  }
}

.event {
  a {
    display: flex;
    justify-content: space-between;
    padding: 16px;
    margin-bottom: 2px;
    background-color: $color-grey-lhter;

    &:hover {
      background-color: $color-grey-dsabl;
    }

    .summary {
      display: flex;
      flex-direction: column;
      padding: 8px 16px;

      .tag {
        margin-bottom: 5px;
      }

      .description {
        color: $color-grey-dft;
        font-size: $font-sz-smer;
      }
    }

    .posts {
      display: flex;

      img {
        height: 80px;
        width: 80px;
        padding-left: 2px;
      }
    }
  }
}

</style>
