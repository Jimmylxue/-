<template>
  <div class="listPage">
    <!-- nav -->
    <div class="navcontainer">
      <nav>
      <div class="nav">
        <div><van-icon name="arrow-left" /></div>
        <div>
          <div>福州市</div>
          <div>
            <span><small>住</small>06-09</span><span><small>离</small>06-13</span>
          </div>
          <div>
            <input type="text" placeholder="请输入您要搜索的内容">
          </div>
        </div>
        <div><van-icon name="weapp-nav" /></div>
      </div>
    </nav>
    </div>
    
    <!-- tab -->
    <div class="tab">
      <div>推荐排序</div>
      <div>位置排序<van-icon class="icons" name="arrow-up" /></div>
      <div>价格排序<van-icon class="icons" name="arrow-up" /></div>
      <div>好评优先<van-icon class="icons" name="arrow-up" /></div>
    </div>
    <div class="adver">
      <img src="@/assets/img/hotel/1.png" width="100%" height="100%" alt="">
    </div>
    <list></list>
    <list></list>
    <list></list>
    <list></list>
  </div>
</template>

<script>
import list from '@/components/page/hotel/components/list.vue'
export default {
  components:{
    list
  },
  data(){
    return {

    }
  }
}
</script>

<style lang="less" scoped>
.listPage{
  font-size: 14px;
  height: 100%;
  overflow-y: auto;
}
// nav、
.navcontainer{
  width: 100%;
  height: 45px;
  background-color: #fff;
}
nav{
  width: 100%;
  height: 45px;
  // background-color: skyblue;
  display: flex;
  align-items: center;
  font-size: 12px;
  position: fixed;
  background-color: #fff;
  .nav{
    width: 100%;
    height: 90%;
    display: flex;
    justify-content: space-between;
    &>div:nth-child(1),&>:nth-child(3){
      width: 45px;
      height: 45px;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 20px;
    }
    &>div:nth-child(1){
      color: #B5B5B5;
    }
    &>div:nth-child(3){
      color: #333;
    }
    &>div:nth-child(2){
      display: flex;
      flex-grow: 1;
      align-items: center;
      border-radius: 20px 5px 5px 20px;
      background-color: #F8F8F8;
      align-items: center;
      &>div:nth-child(1){
        color: #00A0E9;
        width: 23%;
        display: flex;
        justify-content: center;
        padding-left: 10px;
      }
      &>div:nth-child(2){
        width: 26%;
        // height: 45px;
        letter-spacing: 1px;
        display: flex;
        flex-direction: column;
        color: #00A0E9;
        align-items: center;
        &>span:nth-child(2){
          margin-top: -8px;
        }
        small{
          color: #333333;
        }
      }
      &>div:nth-child(3){
        height: 35px;
        border-left: 1px solid rgba(112,112,112,.3);
        input{
          width: 100%;
          font-size: 13px;
        }
        // margin-left: 10px;
        padding-left: 10px;
      }
    }
  }
}
// tab
.tab{
  width: 100%;
  height: 40px;
  display: flex;
  // background-color: skyblue;
  align-items: center;
  font-size: 12px;
  div{
    flex-grow: 1;
    display: flex;
    height: 20px;
    justify-content: center;
    align-items: center;
    color: #333333;
    border-right: 1px solid #B5B5B5;
    line-height: 20px;
    .icons{
      margin-left: 2px;
      padding-bottom: 2px;
    }
  }
  &>div:nth-child(4){
    border-right: none;
  }
}
// adver
.adver{
  margin: 0 auto;
  width: 95%;
  height: 85px;
}
</style>