<template>
  <div>
    <!--首页-搜索框start-->
    <div class="search-bar">
      <div class="search-bar-warpper">
        <van-icon name="search" class="icon" size="15" color="#BBBBBB"/>
        <input
          :focus="focus"
          :disabled="disabled"
          :maxlength="limit"
          :placeholder = "hotSearch.length === 0 ?'请输入':hotSearch"
          @input="onChange"
          v-model="searchWord"
          placeholder-style="color: #ccc"
          />
        <van-icon name="clear" class="icon" size="15" color="#ccc" @click="onClearClick" v-if="searchWord.length >0 "/>
      </div>
    </div>
    <!--首页-搜索框end-->
  </div>
</template>

<script>
  export default {
    props: {
      focus: {
        type: Boolean,
        default: true
      },
      disabled: {
        type: Boolean,
        default: false
      },
      limit: {
        type: Number,
        default: 50
      },
      hotSearch: {
        type: String,
        default: ''
      }
    },
    data() {
      return {
        searchWord: ''
      }
    },
    methods: {
      onSearchBarClick () {
        console.log('onSearchBarClick搜索框点击事件')
        this.$emit('onClick')
      },
      onClearClick () {
        console.log('清空搜索内容')
        this.searchWord = ''
      },
      onChange (e) {
        const { value } = e.mp.detail
        this.$emit('onChange', value)
      },
      onConfirm(e) {
        const { value } = e.mp.detail
        this.$emit('onConfirm', value)
      },
      setValue (e) {
        this.searchWord = e
      },
      getValue (v) {
        this.searchWord = v
      }
    }
  }
</script>

<style scoped>
  .search-bar{
    padding: 15px 15px;
  }
  .search-bar-warpper{
    display: flex;
    align-items: center;
    background: #F5F7F9;
    box-sizing: border-box;
    border-radius: 20px;
    height: 40px;
    padding: 12px 17px;
  }
  .search-bar input{
    flex:1;
    background: #F5F7F9;
    margin: 0 12px;
    font-size: 14px;
  }
  .icon{
    display: flex;
    align-items: center;
    height: 100%;
    /*padding: 0 16px 0 16px;*/
  }
</style>
