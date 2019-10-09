<template>
    <div class="image-view" @click="onClick">
      <div class="image">
      <img
        :class="round ? 'round image' : 'image' "
        :style="{ height }"
        :src="src"
        :mode="mode"
        :lazy-load="lazyLoad"
        :show-menu-by-longpress="true"
        @load="onLoad"
        @error="onError"
        v-show="!isLoading && !error"
      />
      <img
        :class="round ? 'round image' : 'image' "
        :style="{ height }"
        src="https://www.youbaobao.xyz/book/img/loading2.ae9e5924.jpeg"
        :mode="mode"
        :lazy-load="lazyLoad"
        :show-menu-by-longpress="true"
        @load="onLoad"
        @error="onError"
        v-show="isLoading || error"
      />
    </div></div>
</template>

<script>
  export default {
    props: {
      src: {
        type: String,
        default: ''
      },
      mode: {
        type: String,
        default: 'widthFix'
      },
      lazyLoad: {
        type: Boolean,
        default: true
      },
      round: {
        type: Boolean,
        default: false
      },
      height: {
        type: String,
        default: 'auto'
      }
    },
    watch: {
      src(newValue, preValue) {}
    },
    data() {
      return {
        isLoading: true,
        error: false
      }
    },
    methods: {
      onClick() {
        console.log('onClick')
        this.$emit('onClick')
      },
      onLoad() {
        //  图片加载成功后
        console.log('onLoad')
        this.isLoading = false
        this.error = false
      }
    }
  }
</script>

<style lang="scss" scoped>
  .image-view {
    width: 100%;
  }
  .demo {
    display: flex;
    align-items: center;
  }
  .image {
    width: 100%;
    &.round {
      border-radius: 50%;
     }
  }
</style>
