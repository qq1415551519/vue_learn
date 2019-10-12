<template>
    <div class="home-card">
      <div class="home-card-inner">
        <div class="user-info">
          <div class="user-avatar">
            <ImageView
              src="https://www.youbaobao.xyz/mpvue-res/logo.jpg"
              round
            ></ImageView>
          </div>
          <div class="user-nick-name">米老鼠</div>
          <div class="book-text">书架共有搜素 </div>
          <div class="round-spot"></div>
          <div class="book-text" @click="gotoShelf">特别精选</div>
        </div>
        <div class="book-info">
          <div class="book-wrapper">
            <div class="book-img-wrapper">
              <ImageView
                src="https://www.youbaobao.xyz/book/res/img//EarthSciences/978-981-10-3713-9_CoverFigure.jpg"
              ></ImageView>
            </div>
            <div class="book-img-wrapper">
              <ImageView
                src="https://www.youbaobao.xyz/book/res/img//EarthSciences/978-981-10-3713-9_CoverFigure.jpg"
              ></ImageView>
            </div>
            <div class="book-img-wrapper">
            <ImageView
              src="https://www.youbaobao.xyz/book/res/img//EarthSciences/978-981-10-3713-9_CoverFigure.jpg"
            ></ImageView>
            </div>

          </div>
          <div class="shelf_wrapper">
            <div>书架</div>
          </div>
        </div>
        <div >
          <div class="feedback-wrapper">
          </div>
          <div class="feedback-wrapper-text" @click="demo">
            反馈
          </div>
        </div>
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
      },
      demo() {
        console.log('555555')
      }
    }
  }
</script>

<style lang="scss" scoped>
  .home-card{
    background-image: linear-gradient(-90deg, #54575F 0%, #595B60 100%);
    margin: 20px 20px 0px 20px;
    border-radius: 30px;
    .home-card-inner{
      padding: 20px 20px 10px 20px;
      box-sizing: border-box;
      .user-info{
        display: flex;
        align-items: center;
        .user-avatar{
          width: 20px;
          height: 20px;
        }
        .user-nick-name{
          font-family: PingFangSC-Regular;
          font-size: 16px;
          color: #FFFFFF;
          text-align: center;
          margin: 0 5px;
        }
        .round-spot{
          background-color: #FFFFFF;
          width: 4px;
          height: 4px;
          border-radius: 50%;
        }
        .book-text{
          opacity: 0.7;
          font-family: PingFangSC-Regular;
          font-size: 14px;
          color: #FFFFFF;
          text-align: center;
          margin: 0 8px;
        }
      }
      .book-info{
        display: flex;
        /*background-color: aqua;*/
        .book-wrapper{
          display: flex;
          align-items: center;
          width: 250px;
          height: 120px;
          /*background-color: red;*/
          padding-right: 5px;
          padding-top: 10px;
          justify-content: space-around;
          .book-img-wrapper{
            width: 72px;
            height: 101px;
          }
        }
        .shelf_wrapper{
          display: flex;
          align-items: center;
          /*opacity: 0.8;*/
          font-family: PingFangSC-Regular;
          width: 18px;
          font-size: 14px;
          color: #FFFFFF;
          text-align: center;
        }
      }
      .feedback-wrapper{
        position: absolute;
        opacity: 0.3;
        background: #D8D8D8;
        border-radius: 200px 0 0 200px;
        width: 44px;
        height: 23px;
        right: 20px;
        top: 130px;
      }
      .feedback-wrapper-text{
        position: absolute;
        width: 44px;
        height: 23px;
        right: 20px;
        top: 132px;
        color: #fff;
        font-family: PingFangSC-Regular;
        font-size: 12px;
        text-align: center;
      }
    }
  }

</style>
