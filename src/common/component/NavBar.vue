<template>
  <section class="wrapper">
    <div class="nav-wrapper">
      <router-link tag="div" class="item" to="/home">
        <span>首页</span>
      </router-link>
      <router-link tag="div" class="item" to="/technologySystem">
        <span>体系</span>
      </router-link>
      <router-link tag="div" class="item" to="/project">
        <span>项目</span>
      </router-link>
      <router-link tag="div" class="item" to="/collection" v-show="showCollection">
        <span>收藏</span>
      </router-link>
    </div>
  </section>
</template>

<script>
  export default {
    props: {
      showCollection: {
        type: Boolean,
        default: false
      }
    },
    name: 'nav-bar'
  };
</script>

<style scoped lang="scss">
  @import "../css/constant";

  .wrapper {
    box-sizing: border-box;
    width: 100%;
    height: $navBarHeight;
    line-height: $navBarHeight;
    .nav-wrapper {
      display: flex;
      flex-direction: row;
      width: 200px;
      margin: 0 auto;
      border: 1px solid $bgColor;
      border-radius: 4px;
      background: $bgColor;
      .item {
        font-size: $fontSize;
        flex-grow: 1;
        text-align: center;
        &.router-link-active span {
          color: #ffffff;
        }
      }
    }

  }
</style>
