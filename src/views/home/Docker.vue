<template>
  <div class='docker'>
    <div
      v-for="(item, index) in dockerList"
      :key="index"
      :class="{'docker__item': true, 'docker__item--active': index === 0}"
    >
      <div class="iconfont" v-html="item.icon"></div>
      <div class="docker__title">{{item.text}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DockerPage',
  setup () {
    const dockerList = [
      { icon: '&#xe648;', text: '首页' },
      { icon: '&#xe634;', text: '购物车' },
      { icon: '&#xe6ab;', text: '订单' },
      { icon: '&#xe660;', text: '我的' }
    ]
    return { dockerList }
  }
}
</script>

<style lang="scss" scoped>
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
