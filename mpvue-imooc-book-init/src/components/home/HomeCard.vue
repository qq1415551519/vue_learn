<template>
    <div class="home-card">
      <div class="home-card-inner">
        <div class="user-info">
          <ImageView
          src="http://api.myphp.vip/bizhi001.png"
          height="200px;"
          mode="scaleToFill"
          ></ImageView>
        </div>
        <div class="book-info">2019</div>
        <div class="feedback-wrapper"></div>
      </div>
    </div>
</template>

<script>
  import ImageView from '../base/imageView'
  export default {
    components: { ImageView },
    props: {
      data: Object,
      hasSign: {
        type: Boolean,
        default: false
      },
      signDay: {
        type: Number,
        default: 0
      }
    },
    method: {
      gotoShelf() {
        console.log('gotoShelf')
      },
      onBookClick() {
        console.log('onBookClick')
      },
      sign() {
        console.log('sign')
      }
    }
  }
</script>

<style scoped>
</style>
