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
      <div class="icons__item">
        <img src="http://www.dell-lee.com/imgs/vue3/超市.png" alt="" class="icons__item__icon">
        <p class="icons__item__desc">超市遍历</p>
      </div>
      <div class="icons__item">
        <img src="http://www.dell-lee.com/imgs/vue3/菜市场.png" alt="" class="icons__item__icon">
        <p class="icons__item__desc">菜市场</p>
      </div>
      <div class="icons__item">
        <img src="http://www.dell-lee.com/imgs/vue3/水果店.png" alt="" class="icons__item__icon">
        <p class="icons__item__desc">水果店</p>
      </div>
      <div class="icons__item">
        <img src="http://www.dell-lee.com/imgs/vue3/鲜花.png" alt="" class="icons__item__icon">
        <p class="icons__item__desc">鲜花绿植</p>
      </div>
      <div class="icons__item">
        <img src="http://www.dell-lee.com/imgs/vue3/医药健康.png" alt="" class="icons__item__icon">
        <p class="icons__item__desc">医药健康</p>
      </div>
      <div class="icons__item">
        <img src="http://www.dell-lee.com/imgs/vue3/家居.png" alt="" class="icons__item__icon">
        <p class="icons__item__desc">家居时尚</p>
      </div>
      <div class="icons__item">
        <img src="http://www.dell-lee.com/imgs/vue3/蛋糕.png" alt="" class="icons__item__icon">
        <p class="icons__item__desc">烘焙蛋糕</p>
      </div>
      <div class="icons__item">
        <img src="http://www.dell-lee.com/imgs/vue3/签到.png" alt="" class="icons__item__icon">
        <p class="icons__item__desc">签到</p>
      </div>
      <div class="icons__item">
        <img src="http://www.dell-lee.com/imgs/vue3/大牌免运.png" alt="" class="icons__item__icon">
        <p class="icons__item__desc">大牌免运</p>
      </div>
      <div class="icons__item">
        <img src="http://www.dell-lee.com/imgs/vue3/红包.png" alt="" class="icons__item__icon">
        <p class="icons__item__desc">红包套餐</p>
      </div>
    </div>
    <div class="gap"></div>
</template>

<script>
export default {
  name: 'StaticPart'
}
</script>

<style lang="scss" >
@import '../../style/viriables.scss';
@import '../../style/mixins.scss';
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
      right: .2rem;
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
