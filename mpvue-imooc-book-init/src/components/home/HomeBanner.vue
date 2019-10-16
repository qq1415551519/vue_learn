<template>
    <div class="home-banner">
      <ImageView
        :src="img"
      ></ImageView>
      <div>title</div>
      <input value=":title">
    </div>
</template>

<script>
  import ImageView from '../base/imageView'
  export default {
    components: {ImageView},
    props: {
      img: String,
      title: String,
      subTitle: String
    },
    methods: {
      onClick() {
        console.log('4444')
      }
    }
  }
</script>

<style scoped>

</style>
