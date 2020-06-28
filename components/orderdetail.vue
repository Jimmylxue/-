<template>
  <div class="orderdetail alluse">
    <van-nav-bar
      title="订单详情"
      left-text=""
      right-text=""
      left-arrow
      @click-left="onClickLeft"
    />
    <div class="card">
      <div>
        <div class="img">
          <img src="@/assets/img/hotel/i1.png" width="100%" height="100%" alt="">
        </div>
        <div class="msg">
          <p>如家福州金融界万达广场店</p>
          <p>经典海景大床房</p>
          <p style="margin-left:-5px">【35m²  |  1.8m大床  |  带窗  |  小花园】</p>
        </div>
      </div>
      <div>
        <van-icon class="icon" name="calender-o" />
        06月15日 星期一 ~ 06月16日 星期二 | 住1晚
      </div>
    </div>
    <div class="check">
      <div>
        <div>
          <div>入住时间</div>
          <div><span>01月26日</span><span>--</span></div>
        </div>
        <div>
          <div>离店时间</div>
          <div><span>01月29日</span><span>共1间3晚</span></div>
        </div>
      </div>
      <div>
        <div>
          <div>入住人</div>
          <div><span>某某某</span></div>
        </div>
        <div>
          <div>联系手机</div>
          <div><span>159****5672</span></div>
        </div>
      </div>
    </div>
    <div class="check">
      <div>
        <div>
          <div>订单号</div>
          <div><span>107698836095342654</span></div>
        </div>
      </div>
      <div>
        <div>
          <div>下单时间</div>
          <div><span>2020/06/07 13:23:31</span></div>
        </div>
      </div>
      <div>
        <div>
          <div>支付方式</div>
          <div><span>支付宝支付</span></div>
        </div>
      </div>
      
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="less" scoped>
.orderdetail{
  font-size: 14px;
  height: 100vh;
  background-color: rgba(243,243,243,1);
}
.card{
  width: 100%;
  // height: 120px;
  margin: 0 auto;
  background-color: #fff;
  border-radius: 5px;
  padding: 10px 10px 5px 10px;
  // z-index: 5;
  &>div:nth-child(1){
    display: flex;
    height: 75px;
    align-items: center;
    border-bottom: 1px solid rgba(112,112,112,.1);
    padding-bottom: 10px;
    .img{
      width: 60px;
      height: 60px;
    }
    .msg{
      flex-grow: 1;
      padding-left: 10px;
      &>p:nth-child(1){
        font-size: 15px;
        color: #333;
        font-weight: bold;
      }
      &>p:nth-child(2){
        font-size: 13px;
        color: #B5B5B5;
      }
      &>p:nth-child(3){
        font-size: 13px;
        color: #B5B5B5;
        display: flex;
        align-items: center;
        span{
          display: inline-block;
          height: 12px;
          line-height: 15px;
          margin-right: 5px;
          border-right: 1px solid #B5B5B5;
          padding-right: 5px;
          &:first-child{
            margin-bottom: 10px;
            border-right: none;
          }
          &:nth-child(2){
            // border-right: none;
            padding-left: 5px;
            border-left: 1px solid #B5B5B5;
          }
        }
        &>span:last-child{
          margin-right: 0;
          border-right: none;
        }
      }
    }
  }
  &>div:nth-child(2){
    display: flex;
    // padding-top: 5px;
    align-items: center;
    color: #333;
    padding: 2px 0;
    .icon{
      margin-right: 5px;
      transform: scale(1.2);
    }
  }
}
.check{
  width: 100%;
  background-color: #fff;
  padding: 0 10px;
  margin-top: 10px;
  &>div{
    padding: 5px 0;
  }
  &>div:nth-child(1){
    display: flex;
    flex-direction: column;
    border-bottom: 1px solid rgba(112,112,112,.1);
    &>div:nth-child(1){
      display: flex;
      &>div:nth-child(1){
        width: 25%;
        color: #B5B5B5;
      }
      &>div:nth-child(2){
        width: 75%;
        color: #333333;
        span{
          margin-right: 20px;
        }
      }
    }
    &>div:nth-child(2){
      display: flex;
      &>div:nth-child(1){
        width: 25%;
        color: #B5B5B5;
      }
      &>div:nth-child(2){
        width: 75%;
        color: #333333;
        span{
          margin-right: 20px;
        }
      }
    }
  }
  &>div:nth-child(3){
    display: flex;
    flex-direction: column;
    border-top:1px solid rgba(112,112,112,.1) ;
    &>div:nth-child(1){
      display: flex;
      &>div:nth-child(1){
        width: 25%;
        color: #B5B5B5;
      }
      &>div:nth-child(2){
        width: 75%;
        color: #333333;
        span{
          margin-right: 20px;
        }
      }
    }
    &>div:nth-child(2){
      display: flex;
      &>div:nth-child(1){
        width: 25%;
        color: #B5B5B5;
      }
      &>div:nth-child(2){
        width: 75%;
        color: #333333;
        span{
          margin-right: 20px;
        }
      }
    }
  }
  &>div:nth-child(2){
    display: flex;
    flex-direction: column;
    &>div:nth-child(1){
      display: flex;
      &>div:nth-child(1){
        width: 25%;
        color: #B5B5B5;
      }
      &>div:nth-child(2){
        width: 75%;
        color: #333333;
        span{
          margin-right: 20px;
        }
      }
    }
    &>div:nth-child(2){
      display: flex;
      &>div:nth-child(1){
        width: 25%;
        color: #B5B5B5;
      }
      &>div:nth-child(2){
        width: 75%;
        color: #333333;
        span{
          margin-right: 20px;
        }
      }
    }
  }
}
</style>