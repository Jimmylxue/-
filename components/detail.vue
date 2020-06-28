<template>
  <div class="detail">
    <div class="nav">
      <div><van-icon class="icons" name="arrow-left" /></div>
      <div><van-icon class="icons" name="scan" /></div>
      <div><van-icon class="icons" name="like-o" /></div>
    </div>
    <div class="bg">
      <img src="@/assets/img/hotel/bg.png" width="100%" height="100%" alt="">
      <div class="price">
        最低<span>354</span>元起
      </div>
    </div>
    <div class="name">
      <div>如家福州金融界万达广场店</div>
      <div>
        <span>仅宾馆</span>
        <span>免费停车</span>
        <span>开业特惠</span>
      </div>
    </div>
    <!-- msg -->
    <div class="msg">
      <div>
        <div>
          <van-icon class="icon" name="balance-o" />
          <span>免费早餐</span>
        </div>
        <div>
          <van-icon class="icon" name="balance-o" />
          <span>24小时前台</span>
        </div>
        <div>
          <van-icon class="icon" name="balance-o" />
          <span>免费WIFI</span>
        </div>
        <div>
          <van-icon class="icon" name="balance-o" />
          <span>免费停车</span>
        </div>
        <div>
          <van-icon class="icon" name="balance-o" />
          <span>免费会议室</span>
        </div>
        <div>
          <van-icon class="icon" name="balance-o" />
          <span>行李寄存</span>
        </div>
      </div>
      <div>
        <div>
          <img src="@/assets/img/hotel/address.png" width="100%" height="70px" alt="">
        </div>
        <div>
          <p>福建省福州市台江区排尾路399号(台江万达附近)</p>
          <p>
            <span><van-icon class="icon" name="newspaper-o" />立即导航</span><span><van-icon class="icon" name="phone-circle-o" />咨询客服</span>
          </p>
        </div>
      </div>
    </div>
    <!-- tab -->
    <div class="tab">
      <van-tabs line-width="40px" color="#00A0E9" v-model="active">
        <van-tab title="房型">
          <div class="type">
            <div class="time">
              <span>住</span>
              <span>06-03</span>
              <span>离</span>
              <span>06-12</span>
              <span>9晚</span>
            </div>
            <div class="adver">
              <img src="@/assets/img/hotel/2.png" width="100%" height="100%" alt="">
              <div class="box">
                <div>
                  <p>经典海景大床房</p>
                  <p><span>35m <sup>2</sup></span>
                  <span>1.8m大床</span>
                  <span>带窗</span>
                  <span>小花园</span></p>
                </div>
                <div>
                  VR看房
                </div>
              </div>
            </div>
            <div class="item">
              <div>经典海景大床房</div>
              <div>
                <span>¥566</span><small>已优惠¥90</small>
              </div>
              <div>预定</div>
            </div>
            <div class="item">
              <div>经典海景大床房</div>
              <div>
                <span>¥566</span><small>已优惠¥90</small>
              </div>
              <div>预定</div>
            </div>
            <div class="item">
              <div>经典海景大床房</div>
              <div>
                <span>¥566</span><small>已优惠¥90</small>
              </div>
              <div>预定</div>
            </div>
            <div class="item">
              <div>经典海景大床房</div>
              <div>
                <span>¥566</span><small>已优惠¥90</small>
              </div>
              <div>预定</div>
            </div>
            <div class="item">
              <div>经典海景大床房</div>
              <div>
                <span>¥566</span><small>已优惠¥90</small>
              </div>
              <div>预定</div>
            </div>
            <div class="adver">
              <img src="@/assets/img/hotel/2.png" width="100%" height="100%" alt="">
              <div class="box">
                <div>
                  <p>经典海景大床房</p>
                  <p><span>35m <sup>2</sup></span>
                  <span>1.8m大床</span>
                  <span>带窗</span>
                  <span>小花园</span></p>
                </div>
                <div>
                  VR看房
                </div>
              </div>
            </div>
            <div class="item">
              <div>经典海景大床房</div>
              <div>
                <span>¥566</span><small>已优惠¥90</small>
              </div>
              <div>预定</div>
            </div>
            <div class="item">
              <div>经典海景大床房</div>
              <div>
                <span>¥566</span><small>已优惠¥90</small>
              </div>
              <div>预定</div>
            </div>
            <div class="item">
              <div>经典海景大床房</div>
              <div>
                <span>¥566</span><small>已优惠¥90</small>
              </div>
              <div>预定</div>
            </div>
            <div class="item">
              <div>经典海景大床房</div>
              <div>
                <span>¥566</span><small>已优惠¥90</small>
              </div>
              <div>预定</div>
            </div>
            <div class="item">
              <div>经典海景大床房</div>
              <div>
                <span>¥566</span><small>已优惠¥90</small>
              </div>
              <div>预定</div>
            </div>
          </div>
        </van-tab>
        <van-tab title="概况">内容 2</van-tab>
        <van-tab title="点评">内容 3</van-tab>
      </van-tabs>

    </div>
    <div class="footbar">
      <div>
        <div>最低: <span><small>¥</small>450<small>起</small></span></div>
        <div>
          已享受新注册用户折扣
        </div>
      </div>
      <div>选择房型</div>
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="less" scoped>
.detail{
  font-size: 14px;
  height: 100vh;
  background-color: #F8F8F8;
  height: 100%;
  overflow: auto;
  padding-bottom: 55px;
}
.nav{
  position: fixed;
  z-index: 5;
  top: 0;
  width: 100%;
  height: 45px;
  background-color: transparent;
  display: flex;
  align-items: center;
  padding: 0 10px;
  div{
    width: 30px;
    height: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: rgba(0, 0, 0, .5);
    border-radius: 50%;
    color: #fff;
    &>.icons{
      transform: scale(1.2);
    }
  }
  &>div:nth-child(1){
    margin-right: auto;
  }
  &>div:nth-child(2){
    margin-right: 10px;
  }
}
.bg{
  width: 100%;
  position: relative;
  z-index: 4;
  // height: 100%;
  .price{
    position: absolute;
    left: 10px;
    bottom: -10px;
    width: 115px;
    height: 38px;
    color: #fff;
    text-align: center;
    font-size: 12px;
    border-radius: 5px 0 5px 0;
    background:linear-gradient(57deg,rgba(0,160,233,1) 0%,rgba(119,212,255,1) 100%);
    span{
      font-size: 20px;
    }
  }
}
.name{
  width: 100%;
  height: 90px;
  background-color: #fff;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 0 10px;
  &>div:nth-child(1){
    color: #333333;
    font-size: 18px;
    font-weight: bold;
    margin-top: -5px;
  }
  &>div:nth-child(2){
    // margin-top: 5px;
    span{
      display: inline-block;
      background-color: #EFEFEF;
      color: #333333;
      border-radius: 5px;
      padding: 0 5px;
      font-size: 12px;
      margin-right: 10px;
      margin-top: 5px;
    }
  }
}
.msg{
  width: 100%;
  height: 170px;
  background-color: #fff;
  margin-top: 10px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  &>div:nth-child(1){
    width: 100%;
    height: 80px;
    display: grid;
    grid-template-rows: repeat(2,1fr);
    grid-template-columns: repeat(3,1fr);
    &>div{
      color: #333333;
      display: flex;
      justify-content: flex-start;
      align-items: center;
      padding-left: 10px;
      .icon{
        transform: scale(1.2);
        margin-right: 5px;
      }
    }
  }
  &>div:nth-child(2){
    width: 100%;
    height: 75px !important;
    display: grid;
    grid-template-rows: repeat(1,1fr);
    grid-template-columns: repeat(3,1fr);
    padding-left: 10px;
    &>div:nth-child(1){
      grid-row: 1 / span 1;
      grid-column: 1 / span 1;
      // background-color: skyblue;
    }
    &>div:nth-child(2){
      grid-row: 1 / span 1;
      grid-column: 2 / span 2;
      // background-color: red;
      display: flex;
      flex-direction: column;
      justify-content: space-around;
      padding: 0 10px;
      padding-left: 10px;
      &>p:nth-child(1){
        font-size: 14px;
        color: #333;
        line-height: 20px;
      }
      &>p:nth-child(2){
        display: flex;
        align-items: center;
        font-size: 12px;
        span{
          display: inline-block;
          padding: 0 3px;
          color: #fff;
          display: flex;
          justify-content: center;
          align-items: center;
          border-radius: 5px 0 5px 0;
          .icon{
            margin-right: 2px;
          }
          &:nth-child(1){
            background-color: #00A0E9;
            margin-right: 10px;
          }
          &:nth-child(2){
            background-color: #3EC3FF;
          }
        }
      }
    }
  }
}
.tab{
  margin-top: 10px;
}
.type{
  width: 100%;
  padding-top: 15px;
  background-color: #fff;
  .time{
    width: 223px;
    height: 25px;
    background-color: rgba(0,160,233,1);
    border-radius:5px 0px 5px 0px;
    color: #fff;
    // background-color: #fff;
    font-size: 13px;
    margin: 0 auto;
    margin-bottom: 15px;
    display: flex;
    span{
      display: inline-block;
      flex-grow: 1;
      text-align: center;
      &:nth-child(1){
        padding-left: 10px;
      }
      &:nth-child(5){
        padding-right: 10px;
      }
    }
  }
  .adver{
    width: 95%;
    margin: 0 auto;
    position: relative;
    .box{
      width: 100%;
      height: 40px;
      position: absolute;
      bottom: 0;
      display: flex;
      align-items: center;
      padding: 0 10px;
      background:linear-gradient(180deg,rgba(0,0,0,0) 0%,rgba(84,84,84,1) 100%);
      &>div:nth-child(1){
        margin-right: auto;
        display: flex;
        flex-direction: column;
        justify-content: center;
        &>p:nth-child(1){
          color: #fff;
          font-size: 15px;
        }
        &>p:nth-child(2){
          font-size: 12px;
          color: #B5B5B5;
          margin-top: -10px;
        }
      }
      &>div:nth-child(2){
        width: 67px;
        height: 23px;
        background-color: #00A0E9;
        border-radius: 5px 0px 5px 0px;
        display: flex;
        justify-content: center;
        align-items: center;
        color: #fff;
      }
    }
  }
  
  .item{
    width: 95%;
    height: 50px;
    // background-color: skyblue;
    margin: 0 auto;
    display: flex;
    align-items: center;
    // padding: 15px 0;
    &>div:nth-child(1){
      color: #333;
      font-weight: bold;
      font-size: 15px;
      margin-right: auto;
    }
    &>div:nth-child(2){
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      margin-right: 10px;
      &>span:nth-child(1){
        color: #333;
        font-weight: bold;
        font-size: 14px;
      }
      small{
        color: #B5B5B5;
        font-size: 12px;
        margin-top: -5px;
      }
    }
    &>div:nth-child(3){
      color: #fff;
      background-color: #00A0E9;
      display: flex;
      justify-content: center;
      align-items: center;
      width: 50px;
      height: 22.5px;
      border-radius:5px 0px 5px 0px;
    }
  }
}

.footbar{
  width: 100%;
  height: 50px;
  display: flex;
  align-items: center;
  padding: 0 10px;
  background-color: #fff;
  box-shadow:0px 0px 5px rgba(0,0,0,0.16);
  position: fixed;
  z-index: 5;
  bottom: 0;
  &>div:nth-child(1){
    margin-right: auto;
    &>div:nth-child(1){
      color: #333;

      span{
              font-size: 18px;
        color: #0BB754;
        font-weight: bold;
        small{
          font-size: 12px;
        }
      }
    }
    &>div:nth-child(2){
      color: #B5B5B5;
      font-size: 12px;
      margin-top: -5px;
    }
  }
  &>div:nth-child(2){
    width: 85px;
    height: 30px;
    background-color: #00A0E9;
    color: #fff;
    border-radius:5px 0px 5px 0px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>