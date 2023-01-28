<template>
  <div class="wrapper">
    <div class="position">
      <span class="iconfont position__icon">&#xe9fb;</span>
      北京理工大学国防科技园北京理工大学国防科技园北京理工大学国防科技园
      <span class="iconfont position__notice">&#xe63f;</span>
    </div>
  </div>
  <div class='docker'>
    <div class="docker__item">
      <div class="iconfont docker__item--active">&#xe648;</div>
      <div class="docker__title">首页</div>
    </div>
    <div class="docker__item">
      <div class="iconfont">&#xe634;</div>
      <div class="docker__title">购物车</div>
    </div>
    <div class="docker__item">
      <div class="iconfont">&#xe6ab;</div>
      <div class="docker__title">订单</div>
    </div>
    <div class="docker__item">
      <div class="iconfont">&#xe660;</div>
      <div class="docker__title">我的</div>
    </div>
  </div>
</template>

<style lang="scss">
@import './style/viriables.scss';
@import './style/mixins.scss';
  .wrapper {
    display: flex;
    position: absolute;
    left: 0;
    top: 0;
    bottom: .5rem;
    right: 0;
    padding: 0 .18rem;
  }
  .position {
    position: relative;
    padding: .16rem .24rem .16rem 0;
    line-height: .22rem;
    width : 100%;
    font-size: .16rem;
    color: $content-fontcolor;
    @include ellipsis;
    .position__icon {
      position: relative;
      font-size: .2rem;
      top: .01rem;
    }
    .position__notice {
      position: absolute;
      font-size: .2rem;
      right: 0;
      top: .1rem;
    }
  }
  .docker {
    display: flex;
    position: absolute;
    box-sizing: border-box;
    padding: 0 .18rem;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 0.49rem;
    border-top: 1px solid #F1F1F1;
    color: $content-fontcolor;
    &__item {
      flex : 1;
      text-align: center;
      &--active {
        color: #1FA4FC;
      }
    };
    &__title {
      font-size : 0.2rem;
      transform: scale(0.5, 0.5);
      transform-origin: center top ;
    }
  };
  .iconfont {
    padding: .07rem 0 .02rem 0;
  };
</style>
