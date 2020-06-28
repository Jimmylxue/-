<template>
  <div class="reserve">
    <div class="bg">
      <div class="small">

      </div>
      <van-nav-bar
        title="预定"
        left-text=""
        left-arrow
        @click-left="onClickLeft"
        @click-right="onClickRight"
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
    <div class="checkin">
      <h3>入住信息</h3>
      <div class="cell">
        <div>房间数</div>
        <div>1间<span>每间最多住2人</span></div>
        <div><van-icon name="arrow" /></div>
      </div>
      <div class="cell">
        <div>入住人</div>
        <div><input type="text" placeholder="请输入实际入住人姓名"></div>
      </div>
      <div class="cell">
        <div>手机号</div>
        <div><input type="text" placeholder="用于接收确认短信"></div>
      </div>
      <div style="border-bottom:none" class="cell">
        <div>到店时间</div>
        <div>
          <div @click="showmsg" class="msg">
            <p>14:00后办理入住</p>
            <p>酒店将为您整完保留房间</p>
          </div>
        </div>
      </div>
    </div>
    <div class="quan checkin">
      <h3>优惠券</h3>
      <div class="cell">
        <div>房间数</div>
        <div><span>有两张优惠券可用</span></div>
        <div><van-icon name="arrow" /></div>
      </div>
      <div style="border-bottom:none" class="cell">
        <div>特殊要求</div>
        <div><input type="text" placeholder="请输入您的特别要求"></div>
      </div>
    </div>
    <div class="tag">
      <p>备注:</p>
      <p>1、平台只对任务单价范围做出担保，如产生额外费用或纠纷。平台概不负责，您接单即表示同意并遵守上述准则否则请勿接单。如果任务有违法行为请进行举报。</p>
      <p>2、平台禁止任何形式的线下交易，一经查实立即冻结相关账号，余额不予返还，并给予举报者奖励</p>
    </div>
    <div class="footbar">
      <div>
        <p>总计:<span>¥<strong>450</strong></span></p>
        <p>开通会员即代表接受《会员服务协议》</p>
      </div>
      <div>
        确认支付
      </div>
    </div>
    <div v-show="flag" class="timepick">
      <van-datetime-picker
        v-model="currentTime"
        type="time"
        title="选择时间"
        :min-hour="10"
        :max-hour="20"
        @confirm = "confirm"
      />
    </div>
    
  </div>
    </div>
    
</template>

<script>
export default {
  data(){
    return {
      currentTime: '12:00',
      flag:false
    }
  },
  methods:{
    onClickLeft(){},
    onClickRight(){},
    showmsg(){
      this.flag = true
    },
    confirm(){
      // alert('ok')
      this.flag = false
    }
  }
}
</script>

<style lang="less" scoped>
.reserve{
  font-size: 14px;
  // position: relative;
  height: 100%;
  background: rgba(250,250,250,1);
  z-index: 3;
  overflow: auto;
  position: relative;
  .timepick{
    position: absolute;
    width: 100%;
    top: 60%;
    left: 50%;
    transform: translate(-50%,-50%);
  }
  .bg{
    width: 100%;
    height: 100%;
    // background:linear-gradient(180deg,rgba(0,160,233,1) 0%,rgba(110,197,236,0) 100%);
    position: fixed;
    top: 0;
    overflow: auto;
    z-index: 0;
    padding-bottom: 50px;
    .small{
      width: 100%;
      height: 240px;
      background:linear-gradient(180deg,rgba(0,160,233,1) 0%,rgba(110,197,236,0) 100%);
      position: absolute;
      top: 0;
      z-index: -1;
    }
  }
}
.card{
  width: 95%;
  // height: 120px;
  margin: 0 auto;
  background-color: #fff;
  border-radius: 5px;
  padding: 10px 10px 0 10px;
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
.checkin{
  width: 95%;
  // height: 253px;
  background-color: #fff;
  margin: 0 auto;
  margin-top: 10px;
  border-radius: 5px;
  padding: 0 10px;
  // font-size: 14px;
  // background-color: skyblue;
  h3{
      font-size: 15px;
      padding-top: 5px;
      margin-bottom: -5px;
    }
  .cell{
    width: 100%;
    height: 50px;
    display: flex;
    align-items: center;
    border-bottom: 1px solid rgba(112,112,112,.1);
    font-size: 14px;
    color: #333333;
    
    &>div:nth-child(1){
      width: 75px;
    }
    &>div:nth-child(2){
      margin-right: auto;
      span{
        color: #B5B5B5;
        margin-left: 5px;
      }
      input{
        color: #B5B5B5;
        margin-left: 5px;
        &::placeholder{
          color: #B5B5B5;
        }
      }
      .msg{
        display: flex;
        flex-direction: column;
        justify-content: center;
        font-size: 13px;
        color: #333333;
        &>p:nth-child(2){
          color: #B5B5B5;
          margin-top: -5px;
        }
      }
    }
    &>div:nth-child(3){
      color: #B5B5B5;
    }
  }
}
.tag{
  width: 95%;
  height: 158px;
  margin: 0 auto;
  font-size: 13px;
  margin-top: 20px;
  p{
    color: #333333;
  }
  &>p:nth-child(1){
    color: #FF0000;

  }
}

.footbar{
  width: 100%;
  height: 50px;
  background:rgba(255,255,255,1);
  box-shadow:0px 0px 5px rgba(0,0,0,0.16);
  display: flex;
  position: fixed;
  bottom: 0;
  &>div:nth-child(1){
    margin-right: auto;
    padding-left: 10px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    &>p:nth-child(1){
      color: #333;
      display: flex;
      align-items: center;
      span{
        color: #0BB754;
        margin-left: 8px;
        strong{
          font-size: 16px;
        }
      }
    }
    &>p:nth-child(2){
      color: #B5B5B5;
      font-size: 12px;
      margin-top: -5px;
    }
  }
  &>div:nth-child(2){
    width: 120px;
    height: 50px;
    background:linear-gradient(96deg,rgba(0,160,233,1) 0%,rgba(78,200,255,1) 100%);
    font-size: 16px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #fff;
  }
}
</style>