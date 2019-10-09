<template>
  <div>
    <!--搜素-->
    <SearchBar
      :disabled="false"
      :onclick="onSearchBarkClick"
    ></SearchBar>

    <!--读书卡片组件-->
    <HomeCard></HomeCard>
    <!--图片-->
  </div>
</template>

<script>
  import SearchBar from '../../components/home/SearchBar'
  import ImageView from '../../components/base/imageView'
  import { post } from '@/utils/request'
  import HomeCard from '../../components/home/HomeCard'
  export default {
    components: {
      HomeCard,
      SearchBar,
      ImageView
    },
    methods: {
      onSearchBarkClick () {
        console.log('进入搜索页面')
      },
      onClick () {
        console.log(5)
        this.$router.push('/pages/index/main')
      },
      onUrl () {
        console.log(53)
        post('https://baidu.com').then(response => {
          console.log(6)
        })
      }
    }
  }
</script>

<style lang="scss" scoped>
  .book {
    background-image: linear-gradient(-90deg, #54575F 0%, #595B60 100%);
    border-radius: 30px;
    margin: 20px 20px;
  }
  .book-top {
    background-color: aquamarine;
    padding-top: 5px;
  }
</style>
