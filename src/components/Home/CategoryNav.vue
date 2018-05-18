<template>
  <aside>
    <ul class="cat-normal">
      <li class="cat-item">
        <a class="cat-link" href=""><i class="cat-icon"></i><span class="cat-name">家常菜</span></a>
      </li>
      <li class="cat-item">
        <a class="cat-link" href=""><i class="cat-icon"></i><span class="cat-name">快手菜</span></a>
      </li>
      <li class="cat-item">
        <a class="cat-link" href=""><i class="cat-icon"></i><span class="cat-name">下饭菜</span></a>
      </li>
      <li class="cat-item">
        <a class="cat-link" href=""><i class="cat-icon"></i><span class="cat-name">早餐</span></a>
      </li>
      <li class="cat-item">
        <a class="cat-link" href="">
          <i class="cat-icon"></i><span class="cat-name">肉</span><i class="arrow-right"></i>
        </a>
        <div class="cat-subnav"></div>
      </li>
      <li class="cat-item">
        <a class="cat-link" href=""><i class="cat-icon"></i><span class="cat-name">鱼</span></a>
      </li>
      <li class="cat-item">
        <a class="cat-link" href="">
          <i class="cat-icon"></i><span class="cat-name">蔬菜</span><i class="arrow-right"></i>
        </a>
        <div class="cat-subnav">
          <div class="sub-nav-row"></div>
          <div class="sub-nav-row"></div>
          <div class="sub-nav-row"></div>
          <div class="sub-nav-row"></div>
          <div class="sub-nav-row"></div>
        </div>
      </li>
      <li class="cat-item">
        <a class="cat-link" href=""><i class="cat-icon"></i><span class="cat-name">鸡蛋</span></a>
      </li>
      <li class="cat-item">
        <a class="cat-link" href=""><i class="cat-icon"></i><span class="cat-name">汤羹</span></a>
      </li>
      <li class="cat-item">
        <a class="cat-link" href=""><i class="cat-icon"></i><span class="cat-name">烘焙</span></a>
      </li>
      <li class="cat-item">
        <a class="cat-link" href=""><i class="cat-icon"></i><span class="cat-name">主食</span></a>
      </li>
      <li class="cat-item">
        <a class="cat-link" href=""><i class="cat-icon"></i><span class="cat-name">面</span></a>
      </li>
      <li class="cat-item">
        <a class="cat-link" href=""><i class="cat-icon"></i><span class="cat-name">素食</span></a>
      </li>
    </ul>
    <div class="cat-divider"></div>
    <ul class="cat-special">
      <li class="cat-item">
        <a class="cat-link" href=""><i class="cat-icon"></i><span class="cat-name">孕妇</span></a>
      </li>
      <li class="cat-item">
        <a class="cat-link" href=""><i class="cat-icon"></i><span class="cat-name">产妇</span></a>
      </li>
      <li class="cat-item">
        <a class="cat-link" href=""><i class="cat-icon"></i><span class="cat-name">婴儿</span></a>
      </li>
      <li class="cat-item">
        <a class="cat-link" href=""><i class="cat-icon"></i><span class="cat-name">儿童</span></a>
      </li>
    </ul>
    <button class="btn-txt">全部菜谱分类</button>
  </aside>
</template>

<script>
export default {
  name: 'CategoryNav'
}
</script>

<style lang="scss" scoped>
$list-dist: 10px;

aside {
  min-width: 130px;
  font-size: $font-sz-md;

  .cat-item {
    position: relative;
    padding: 0 5px $list-dist 0;

    &:hover {
      .cat-link {
        color: $color-red-dft;
      }

      .arrow-right {
        border-color: $color-grey-dft;
      }

      .cat-subnav {
        display: block;
      }
    }

    .cat-link {
      position: relative;
      display: block;
      transition: .1s;

      .cat-icon {
        display: inline-block;
        width: 32px;
        height: 32px;
        margin-right: 16px;
        background: none no-repeat 0;
        background-image: url(../../assets/cat-icon.png);
        text-indent: 56px;
        vertical-align: middle;
      }

      .cat-name {
        vertical-align: middle;
      }

      .arrow-right {
        transition: .1s;
      }
    }

    .cat-subnav {
      position: absolute;
      display: none;
      top: -15px;
      left: 130px;
      min-height: 100px;
      min-width: 300px;
      padding: 16px 32px;
      bac1kground-color: $color-grey-lhter;

      .cat-subnav-row {
      }
    }
  }

  .cat-divider {
    margin-bottom: $list-dist;
    border-bottom: $border;
  }

  .btn-txt {
    margin-top: 22px;
    color: $color-red-dft;
    font-size: $font-sz-dft;
  }
}

@for $i from 1 through 13 {
  .cat-normal .cat-item:nth-child(#{$i}) {

    .cat-icon {
      background-position: 0 #{-40 * ($i - 1)}px;
    }
  }
}

@for $i from 1 through 4 {
  .cat-special .cat-item:nth-child(#{$i}) {

    .cat-icon {
      background-position: 0 #{-560 + -40 * ($i - 1)}px;
    }
  }
}

</style>
