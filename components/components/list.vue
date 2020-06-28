<template>
  <div class="list">
    <div class="item">
      <div>
        <div>
          <img src="@/assets/img/hotel/i1.png" width="100%" height="" alt="">
        </div>
        <div>
          <p>如家福州金融界万达广场店</p>
          <p>
            <span>4.8分</span><span>2378条评论</span>
          </p>
          <p>福州市排尾路399号(台江万达附近)</p>
          <p>
            <span>距您3公里</span><span><small>¥</small>450<small>起</small></span>
          </p>
        </div>
      </div>
      <div>
        <span>仅宾馆</span>
        <span>免费停车</span>
        <span>开业特惠</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="less" scoped>
.list{
  font-size: 14px;
  width: 100%;
}
.item{
  width: 95%;
  margin: 0 auto;
  padding-bottom: 10px;
  padding-top: 8px;
  border-bottom: 1px solid rgba(112,112,112,.1);;
  // height: 200px;
  // background-color: skyblue;
  &>div:nth-child(1){
    display: flex;
    &>div:nth-child(1){
      width: 32%;
      // background-color: red;
    }
    &>div:nth-child(2){
      padding-left: 10px;
      flex-grow: 1;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      // background-color: skyblue;
      &>p:nth-child(1){
        color: #333;
        font-size: 15px;
        font-weight: bold;
      }
      &>p:nth-child(2){
        font-size: 13px;
        &>span{
          display: inline-block;
        }
        &>span:nth-child(1){
          background-color: #00A0E9;
          border-radius: 5px 0 5px 0;
          color: #fff;
          padding: 0px 3px;
          margin-right: 10px;
        }
        &>span:nth-child(2){
          color: #333333;
          // font-size: 13px;
        }
      }
      &>p:nth-child(3){
        color: #333333;
      }
      &>p:nth-child(4){
        display: flex;
        font-size: 12px;
        align-items: center;
        justify-content: space-between;
        &>span:nth-child(1){
          color: #B5B5B5;
        }
        &>span:nth-child(2){
          color: #0BB754;
          font-size: 16px;
          small{
            font-size: 12px;
          }
        }
      }
    }
  }
  &>div:nth-child(2){
    margin-top: 5px;
    span{
      display: inline-block;
      background-color: #EFEFEF;
      color: #333333;
      border-radius: 5px;
      padding: 0 5px;
      font-size: 12px;
      margin-right: 10px;
    }
  }
}
</style>