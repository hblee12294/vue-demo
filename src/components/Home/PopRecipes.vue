<template>
  <div class="pop-recipes">
    <div class="title-bar">
      <div class="title-group">
        <h3 class="title">最近流行</h3>
        <a class="btn-txt" href="">全部</a>
      </div>
    </div>
    <ul class="recipe-cards">
      <li class="recipe-card" v-for="(recipe, index) in recipes" :key="index">
        <a href="" :title="recipe.title">
          <img class="recipe-img" :src="recipe.src" :alt="recipe.title">
          <div class="recipe-title">
            <span>{{ recipe.title }}</span>
          </div>
          <div class="recipe-footnote">
            <span class="recipe-author">{{ recipe.author }}</span>
            <span class="recipe-num">{{ recipe.num }} 做过</span>
          </div>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'PopRecipes',
  data () {
    return {
      recipes: [{
        title: '拯救冰箱食物-藜麦煲仔饭',
        src: 'http://s2.cdn.xiachufang.com/790741cdddba4ba0a2b29c1e4b8507ca_1620w_1080h.jpg?imageView2/1/w/235/h/138/interlace/1/q/90',
        href: '',
        author: '晴天小超人',
        num: 1
      }, {
        title: '可能是最好吃的香蕉巧克力蛋糕',
        src: 'http://s1.cdn.xiachufang.com/3bc6c8c488ff11e6b87c0242ac110003_1520w_1008h.jpg@2o_50sh_1pr_1l_235w_138h_1c_1e_90q_1wh',
        href: '',
        author: '加奶不加糖-v',
        num: 6965
      }, {
        title: '墨西哥卷饼',
        src: 'http://s2.cdn.xiachufang.com/f42f7ec089a311e6a9a10242ac110002_854w_640h.jpg?imageView2/1/w/235/h/138/interlace/1/q/90',
        href: '',
        author: '一只梨花压海棠',
        num: 2959
      }, {
        title: '红心火龙果汁奶香刀切小馒头',
        src: 'http://s2.cdn.xiachufang.com/64c609ab111f4bbf94445df5799cf0d3_1440w_1080h.jpg?imageView2/1/w/235/h/138/interlace/1/q/90',
        href: '',
        author: '冇伱灬冇我',
        num: 6
      }, {
        title: '香煎龙利鱼——fit食谱系列',
        src: 'http://s2.cdn.xiachufang.com/c951a60088e111e6b87c0242ac110003_1599w_1066h.jpg?imageView2/1/w/235/h/138/interlace/1/q/90',
        href: '',
        author: 'Jagger秦',
        num: 2056
      }, {
        title: '夏日爽口凉拌毛豆',
        src: 'http://s2.cdn.xiachufang.com/8093446c87bc11e6b87c0242ac110003_2000w_1333h.jpg?imageView2/1/w/235/h/138/interlace/1/q/90',
        href: '',
        author: '走走停停_在路上',
        num: 1332
      }, {
        title: '奶酥软欧包',
        src: 'http://s2.cdn.xiachufang.com/88a6100271da4c31983d561a7c9492e0_1920w_1080h.jpg?imageView2/1/w/235/h/138/interlace/1/q/90',
        href: '',
        author: '拾味爸爸',
        num: 460
      }, {
        title: '凉拌茄子',
        src: 'http://s2.cdn.xiachufang.com/373b400288e411e6a9a10242ac110002_1600w_1067h.jpg?imageView2/1/w/235/h/138/interlace/1/q/90',
        href: '',
        author: '呵呵是吗',
        num: 288
      }, {
        title: '懒汉免炒绿豆沙(绿豆糕)',
        src: 'http://s2.cdn.xiachufang.com/ddd9d7f68bab11e6b87c0242ac110003_3264w_2448h.jpg?imageView2/1/w/235/h/138/interlace/1/q/90',
        href: '',
        author: 'sandcastle',
        num: 473
      }, {
        title: '鱼香茄子',
        src: 'http://s2.cdn.xiachufang.com/ba90059e882811e6a9a10242ac110002_800w_600h.jpg?imageView2/1/w/235/h/138/interlace/1/q/90',
        href: '',
        author: '小番茄食堂',
        num: 3672
      }, {
        title: '猪肉大葱锅贴',
        src: 'http://s2.cdn.xiachufang.com/f4e1e8d887de11e6b87c0242ac110003_600w_400h.jpg?imageView2/1/w/235/h/138/interlace/1/q/90',
        href: '',
        author: '王光光光光',
        num: 957
      }, {
        title: '最简单的甜甜圈制作方法',
        src: 'http://s1.cdn.xiachufang.com/c53b88241d1f11e7947d0242ac110002_800w_800h.jpg@2o_50sh_1pr_1l_235w_138h_1c_1e_90q_1wh',
        href: '',
        author: '柚-子-家',
        num: 177
      }]
    }
  }
}
</script>

<style lang="scss" scoped>
.pop-recipes {
  display: inline-block;
  width: 490px;

  .title-bar {
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
  }
}

.recipe-cards {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;

  .recipe-card {
    width: 235px;
    border: $border;
    margin-bottom: 25px;
    text-align: center;

    &:hover {
      .recipe-img {
        opacity: .9;
      }

      .recipe-title {
        color: $color-red-dft;
      }
    }

    .recipe-title {
      padding: 8px 4px;
      overflow: hidden;
      white-space: nowrap;
      text-align: center;
      text-overflow: ellipsis;
      font-size: $font-sz-lgls;
    }

    .recipe-footnote {
      margin-bottom: 16px;
      color: $color-grey-dft;
      font-size: $font-sz-smer;

      span {
        &:first-child {
          margin-right: 10px;
        }
      }
    }
  }
}

</style>
