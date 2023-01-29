<template>
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

<script>
export default {
  name: 'DockerPage'
}
</script>

<style lang="scss">
@import '../../style/viriables.scss';
@import '../../style/mixins.scss';
.docker {
    display: flex;
    position: absolute;
    box-sizing: border-box;
    padding: 0 .18rem;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 0.49rem;
    border-top: 1px solid $content-background-color;
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
