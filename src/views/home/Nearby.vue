<template>
    <div class="nearby">
      <h2 class="nearby__title">附近店铺</h2>
      <div v-for="(item, index) in nearbyList" :key="index" class="nearby__item">
        <img :src= "item.icon" class="nearby__item__icon">
        <div class="nearby__item__content">
          <div class="nearby__item__content__title">{{item.title}}</div>
          <div class="nearby__item__content__tags">
            <span v-for="(tag, index) in tags" :key="index" class="nearby__item__content__tag">{{tag}}</span>
          </div>
          <div class="nearby__item__content__heightlight">
            {{item.heightlight}}
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'NearbyPage',
  setup () {
    const tags = ['月售', '起送', '基础运费']
    const nearbyList = [
      { id: 1, icon: 'http://www.dell-lee.com/imgs/vue3/near.png', title: '沃尔玛', heightlight: 'VIP尊享满89元减4元运费券（每月3张）' },
      { id: 2, icon: 'http://www.dell-lee.com/imgs/vue3/near.png', title: '沃尔玛', heightlight: 'VIP尊享满89元减4元运费券（每月3张）' }
    ]
    return { tags, nearbyList }
  }
}
</script>

<style lang="scss" scoped>
@import '../../style/viriables.scss';
@import '../../style/mixins.scss';
.nearby {
  &__title {
    height: .25rem;
    width: .72rem;
    font-size: .18rem;
    color: #333333;
    margin: .16rem 0 .02rem 0;
  }
  &__item {
    display: flex;
    padding: .06rem 0 .06rem;
    &__icon {
      height: .56rem;
      width: .56rem;
    }
    &__content {
      flex: 1;
      font-size: .13rem;
      border-bottom: 1px solid $content-background-color;
      padding-bottom: .12rem;
      &__title {
        margin: 0 0 .02rem .16rem;
        font-size: .16rem;
        color: $content-fontcolor;
      }
      &__tags {
        margin: .08rem 0;
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
