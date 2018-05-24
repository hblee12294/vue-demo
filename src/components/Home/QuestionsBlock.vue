<template>
  <div class="questions-block">
    <div class="title-bar">
      <div class="title-group">
        <h3 class="title">厨房问答</h3>
        <a class="btn-txt" href="">全部</a>
      </div>
      <div class="new-salon">
        <a class="btn-txt" href="">发起话题</a>
      </div>
    </div>
    <ul class="questions">
      <li class="question" v-for="(question, index) in questions" :key="index">
        <a href="">{{ question.content }}</a>
        <span class="participants">{{ question.participants }} 参与</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'QuestionsBlock',
  data () {
    return {
      questions: [{
        content: '怎么炒淮山不粘稠？',
        href: '/salon/60719/',
        participants: 26
      }, {
        content: '吐司二发可以用冷藏发酵吗？',
        href: '/salon/60715/',
        participants: 14
      }, {
        content: '茄子怎样做少油又好吃？',
        href: '/salon/60728/',
        participants: 48
      }, {
        content: '全蛋液怎样蒸没有孔而且还能和蒸碗完全脱离开？',
        href: '/salon/60756/',
        participants: 18
      }, {
        content: '有什么蛋糕可以不用烤箱和奶油呢？',
        href: '/salon/60780/',
        participants: 30
      }]
    }
  }
}
</script>

<style lang="scss" scoped>
.questions-block {
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

  .questions {
    .question {
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 36px;

      a {
        &:hover {
          color: $color-red-dft;
        }
      }

      span {
        color: $color-grey-dft;
        font-size: $font-sz-smer;
      }
    }
  }
}

</style>
