<template>
    <div class="position">
      <span class="iconfont position__icon">&#xe9fb;</span>
      中国上海市徐汇区天钥桥路上海游泳馆
      <span class="iconfont position__notice">&#xe63f;</span>
    </div>
    <div class="search">
      <span class="iconfont search__icon">&#xe6ac;</span>
      <input id="search__input" type="search" placeholder="山姆会员商店优惠商品"/>
    </div>
    <div class="banner">
      <img class="banner__image" src="http://www.dell-lee.com/imgs/vue3/banner.jpg"/>
    </div>
    <div class="icons">
      <div class="icons__item" v-for="(item, index) in staticPartList" :key="index">
        <img :src="item.url" class="icons__item__icon">
        <p class="icons__item__desc">{{item.desc}}</p>
      </div>
    </div>
    <div class="gap"></div>
</template>

<script>
export default {
  name: 'StaticPart',
  setup () {
    const staticPartList = [
      { url: 'http://www.dell-lee.com/imgs/vue3/超市.png', desc: '超市遍历' },
      { url: 'http://www.dell-lee.com/imgs/vue3/菜市场.png', desc: '菜市场' },
      { url: 'http://www.dell-lee.com/imgs/vue3/水果店.png', desc: '水果店' },
      { url: 'http://www.dell-lee.com/imgs/vue3/鲜花.png', desc: '鲜花绿植' },
      { url: 'http://www.dell-lee.com/imgs/vue3/医药健康.png', desc: '医药健康' },
      { url: 'http://www.dell-lee.com/imgs/vue3/家居.png', desc: '家居时尚' },
      { url: 'http://www.dell-lee.com/imgs/vue3/蛋糕.png', desc: '烘焙蛋糕' },
      { url: 'http://www.dell-lee.com/imgs/vue3/签到.png', desc: '签到' },
      { url: 'http://www.dell-lee.com/imgs/vue3/大牌免运.png', desc: '大牌免运' },
      { url: 'http://www.dell-lee.com/imgs/vue3/红包.png', desc: '红包套餐' }
    ]
    return { staticPartList }
  }
}
</script>

<style lang="scss" scoped>
@import '../../style/viriables.scss';
@import '../../style/mixins.scss';
.position {
    position: relative;
    padding: .16rem .24rem .16rem 0;
    line-height: .22rem;
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
      right: .1rem;
      top: .1rem;
    }
  }
  .search {
    margin-bottom: .12rem;
    height: .32rem;
    background-color: $content-input-background-color;
    color: #B7B7B7;
    border-radius: 16px;
    font-size: .14rem;
    .search__icon {
      position: relative;
      padding: .08rem .12rem .08rem .16rem;
      font-size: .16rem;
    }
    #search__input {
      border-width: 0;
      background-color: $content-input-background-color;
      font-size: .14rem;
      width: 80%;
      padding: .08rem 0;
      ::placeholder {
        color: #B7B7B7;
        font-size: .14rem;
      }
    }
  }
  .banner {
    height: 0;
    overflow: hidden;
    padding-bottom: 25.4%;
    &__image {
      width: 100%;
    }
  }
  .icons {
    display: flex;
    flex-wrap: wrap;
    margin-top: .16rem;
    &__item {
      width: 20%;
      &__icon {
        display: block;
        width: .4rem;
        height: .4rem;
        margin: 0 auto;
      }
      &__desc {
        text-align: center;
        margin: .06rem 0 .16rem 0;
        color: $content-fontcolor;
      }
    }
  }
  .gap {
    height: .1rem;
    background-color: $content-background-color;
    margin: 0 -.18rem;
  }
  .iconfont {
    padding: .07rem 0 .02rem 0;
  };
</style>
