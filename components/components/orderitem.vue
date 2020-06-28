<template>
    <div class="items">
      <div>
        <span>订单编号：2020061830302145</span><span>已支付</span>
      </div>
      <div>
        <div>
          <img src="@/assets/img/hotel/a1.png" width="100%" height="100%" alt="">
        </div>
        <div>
          <div>{{text | textlimit}}</div>
          <div>
            <p>双早 1间3晚</p>
            <p>入住日期：2018-01-16</p>
            <p>商店日期：2018-01-19</p>
          </div>
        </div>
      </div>
      <div>
          <p>共1件商品 合计<span>¥972.30</span></p>
          <button>删除订单</button>
        </div>
    </div>
</template>

<script>
export default {
  data(){
    return {
      text:'如家福州金融界万达广场店（上海浦东机场川沙迪斯尼店）'
    }
  },
  filters:{
    textlimit(values){
      if(values.length<=30){
        return values
      }
      return values.substring(0,30)+'...'
    }
  }
}
</script>

<style lang="less" scoped>

  .items{
  font-size: 14px;
  padding: 0px 10px 10px 10px;
  padding-bottom: 0;
  background-color: #fff;
  margin-bottom: 5px;
  &>div:nth-child(1){
    display: flex;
    height: 40px;
    align-items: center;
    justify-content: space-between;
    border-bottom: 1px solid rgb(243, 243, 243);
    // padding-bottom: 5px;
  }
  &>div:nth-child(2){
    width: 100%;
    display: flex;
    align-items: center;
    border-bottom: 1px solid rgb(243, 243, 243);
    // margin: 5px 0;
    margin-top: 5px;
    padding-bottom: 5px;
    &>div:nth-child(1){
      width:29%;
      height: 105px;
      // margin-right: 10px;
    }
    &>div:nth-child(2){
      width: 71%;
      padding-left: 10px;
      display: flex;
      flex-direction: column;
      height: 105px;
      justify-content: space-between;
      &>div:nth-child(1){
        color: #333333;
        font-weight: bold;
        line-height: 20px;
        overflow: hidden;
        -webkit-line-clamp: 2;
        text-overflow:ellipsis;
        // // 文本不换行
        // white-space: nowrap;
        // white-space: wrap;
      }
      &>div:nth-child(2){
        color: rgb(161, 161, 161);
        font-size: 12px;
        height: 57px;
        line-height: 22px;
        p{
          margin-top: -5px;
          
        }
        &>p:nth-child(1){
          margin-bottom: 5px;
        }
      }
    }
  }
  &>div:nth-child(3){
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    height: 70px;
    font-size: 13px;
    p{
      color: rgb(34, 34, 34);
      span{
        font-size: 18px;
        margin-left: 2px;
      }
    }
    button{
      width: 75px;
      height: 25px;
      color: rgb(100, 100, 100);
      border: 1px solid rgb(209, 209, 209);
      border-radius: 20px;
      background-color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      // margin-top: -5px;
      // padding-bottom: 20px;
    }
  }
}
</style>