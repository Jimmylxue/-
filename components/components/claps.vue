<template>
  <div class="amsg">
      <header>
        <div><img src="@/assets/img/hotel/header.png" width="100%" height="100%" alt=""></div>
        <div>这是我幸福的起点<div class="fot"></div></div>
      </header>
      <div class="msg">
        <p v-show="moreflage===false">{{text | textlimit}}</p>
        <p v-show="moreflage===true">{{text}}</p>
      </div>
      <p class="seemore" @click="seeAll"><span v-show="moreflage===false">全文</span><span v-show="moreflage===true">收起</span></p>
      <div class="imgcontainer">
        <div class="cont">
          <div>
            <img src="@/assets/img/hotel/pic.png" width="100%" height="100%" alt="">
          </div>
          <div>
            <img src="@/assets/img/hotel/pic.png" width="100%" height="100%" alt="">
          </div>
          <div>
            <img src="@/assets/img/hotel/pic.png" width="100%" height="100%" alt="">
          </div>
          <div>
            <img src="@/assets/img/hotel/pic.png" width="100%" height="100%" alt="">
          </div>
            <div>
            <img src="@/assets/img/hotel/pic.png" width="100%" height="100%" alt="">
          </div>
          <div>
            <img src="@/assets/img/hotel/pic.png" width="100%" height="100%" alt="">
          </div>    <!-- 
          <div>
            <img src="@/assets/img/hotel/pic.png" width="100%" height="100%" alt="">
          </div> -->
        </div>
      </div>
      <div class="do">
        <span><van-icon class="ics" name="aim" />如家福州金融街万达广场店</span><span><van-icon class="ics" name="good-job" /><van-icon class="ics" name="chat" /></span>
      </div>
      <div class="comment">
        <p><span>走一趟上海:</span>入住酒店是下午快五点了。说是能不能将夜宵6:00送过来。</p>
        <p><span>亲爱的</span>回复<span>走一趟上海:</span>入住酒店是下午快五点了。说是能不能将夜宵6:00送过来。</p>
      </div>
    </div>
</template>

<script>
export default {
  data(){
    return {
      titleSelect:1,
      moreflage:false,
      text:'入住酒店是下午快五点了。说是能不能将夜宵6:00送过来。周丽姑娘知道我没有吃晚饭。外边下着大雨出去吃饭不方便。给我准备了一份让我意......l是下午快五点了。说是能不能将夜宵6:00送过来。周丽姑娘知道我没有吃晚饭。外边下着大雨出去吃饭不方便。给我准备了一份让我意'
    }
  },
  filters:{
    textlimit(value){
      return value.substring(0,60)+'...'
    }
  },
  methods:{
    onClickLeft(){},
    seeAll(){
      this.moreflage = !this.moreflage
    }
  }
}
</script>

<style lang="less" scoped>
  .amsg{
  width: 100%;
  // height: 540px;
  font-size: 14px;
  background-color: #fff;
  margin-top: 5px;
  margin-bottom: 8px;
  color: #333;
  padding: 10px 10px;
  header{
    display: flex;
    align-items: center;
    &>div:nth-child(1){
      width: 30px;
      height: 30px;
      border-radius: 50%;
      overflow: hidden;
      margin-right: 10px;
    }
    &>div:nth-child(2){
      font-size: 15px;
      color: #333;
      font-weight: bold;
      position: relative;
      .fot{
        width: 100%;
        height: 5px;
        background-color: #00A0E9;
        position: absolute;
        opacity: 0.5;
        bottom: 6px;
        left: 0;
      }
    }
    // &>div:nth-child(2)::before{
    //   width: 100%;
    //     height: 5px;
    //     background-color: #00A0E9;
    //     position: absolute;
    //     bottom: 0;
    //     left: 0;
    // }
  }
  .msg{
    line-height: 20px;
    margin-top: 8px;
  }
  .seemore{
    color: #0BB754;
  }
  .imgcontainer{
    display: flex;
    flex-wrap: wrap;
    // margin: 0 auto;
    // justify-content: space-between;
    .cont{
      // flex-grow: 0;
      width: 100%;
      margin: 0 auto;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      // justify-content: space-around;
      div{
        width: 32%;
        height: 122px;
        margin-bottom: 5px;
      }
    }
    .cont::after{
      width: 32%;
      content:''
    }
    
  }
  .do{
    display: flex;
    justify-content: space-between;
    margin-top: 5px;
    font-size: 13px;
    &>span:nth-child(1){
      background:rgba(255,213,0,.1);
      color: #333;
      display: flex;
      align-items: center;
      padding: 0 8px;
      .ics{
        margin-right: 5px;
      }
    }
    &>span:nth-child(2){
      .ics{
        margin: 0 5px;
        transform: scale(1.1);
      }
    }
  }
  .comment{
    width: 100%;
    font-size: 13px;
    p{
      color: #333333;
      background-color: rgb(248, 248, 248);
      padding: 0 5px;
      margin-top: 5px;
      span{
        color: #00A0E9;
        margin: 0 2px;
      }
    }
  }
}
</style>