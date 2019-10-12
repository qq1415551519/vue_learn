<template>
    <div class="home-banner"></div>
</template>

<script>
  export default {
    props:{
      img: String,
      title: String,
      subTitle: String,
      }
    },
    methods: {
      onClick() {
        console.log('4444')
        @.$em
      }
    }
  }
</script>

<style scoped>

</style>
