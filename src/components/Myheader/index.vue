<template>
  <header
    class="mint-header"
    :class="{ 'is-fixed': fixed }">
    <div class="mint-header-button is-left">
      <slot name="left"></slot>
    </div>
    <div class="center-wrapper">
      <slot name="center">
        <router-link to="/searchlist">
          <search></search>
        </router-link>
      </slot>
    </div>
    <div class="mint-header-button is-right">
      <slot name="right"></slot>
    </div>
  </header>
</template>

<script>
  /**
   * mt-header
   * @module components/header
   * @desc 顶部导航
   * @param {boolean} [fixed=false] - 固定顶部
   * @param {string} [title] - 标题
   * @param {slot} [left] - 显示在左侧区域
   * @param {slot} [right] - 显示在右侧区域
   *
   * @example
   * <mt-header title="我是标题" fixed>
   *   <mt-button slot="left" icon="back" @click="handleBack">返回</mt-button>
   *   <mt-button slot="right" icon="more"></mt-button>
   * </mt-header>
   */
  export default {
    name: 'mt-header',

    props: {
      fixed: Boolean,
      title: String
    }
  };
</script>

<style scoped lang="scss" rel="stylesheet/scss">
  @import '../../styles/variables';
    header {
    .center-wrapper{
      flex: 2;
    }
  }
</style>
