<template>
    <div class="nearby">
      <h2 class="nearby__title">附近店铺</h2>
      <div class="nearby__item">
        <img src="http://www.dell-lee.com/imgs/vue3/near.png" alt="" class="nearby__item__icon">
        <div class="nearby__item__content">
          <div class="nearby__item__content__title">沃尔玛</div>
          <div class="nearby__item__content__tags">
            <span class="nearby__item__content__tag">月售</span>
            <span class="nearby__item__content__tag">起送</span>
            <span class="nearby__item__content__tag">基础运费</span>
          </div>
          <div class="nearby__item__content__heightlight">
            VIP尊享满89元减4元运费券（每月3张）
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'NearbyPage'
}
</script>

<style lang="scss">
@import '../../style/viriables.scss';
@import '../../style/mixins.scss';
.nearby {
  &__title {
    height: .25rem;
    width: .72rem;
    font-size: .18rem;
    color: #333333;
    margin: .16rem 0 .14rem 0;
  }
  &__item {
    display: flex;
    padding-top: .12rem;
    &__icon {
      height: .56rem;
      width: .56rem;
    }
    &__content {
      flex: 1;
      font-size: .13rem;
      border-bottom: 1px solid $content-background-color;
      padding: .12rem 0;
      &__title {
        margin: 0 0 .08rem .16rem;
        font-size: .16rem;
        color: $content-fontcolor;
      }
      &__tags {
        margin-bottom: .08rem;
      }
      &__tag {
          margin: 0 .16rem 0 .16rem;
      }
      &__heightlight {
          margin-left: .16rem;
          color: #E93B3B;
      }
    }
  }
}

</style>
