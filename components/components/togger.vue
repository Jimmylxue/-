<template>
  <div class="togger">
    <div class="cont">
      <div class="aside_left">
        <img src="@/assets/img/hotel/i1.png" width="100%" height="100%" alt />
      </div>
      <div class="aside_right">
        <div class="head_title">
          <span>福建-福州</span>
          <span>厦门一格·眠宿海景民宿（曾厝垵店）</span>
        </div>
        <div class="site">
          <van-icon class="icon" name="location-o" />福建省福州市排尾路399号(台江万达附近)
        </div>
        <div class="mode">
          <van-icon class="icon" name="wap-home-o" />经典海景大床房双早
        </div>
        <div class="money_foot">
          <div>
            <van-icon class="icon" name="manager-o" />
            <span>
              同住
              <span class="tag">3</span>小时
            </span>
            <span>
              性别：
              <span class="tag">女</span>
            </span>
          </div>
          <div>
            <small>¥</small>70
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="less" scoped>
.togger {
  font-size: 14px;
  width: 100%;
  display: flex;
  margin-bottom: 10px;
  // padding: 0 10px;
  justify-content: center;
  .cont {
    border-bottom: 1px solid rgba(112, 112, 112, 0.1);
    display: flex;
  }
  .aside_left {
    width: 105px;
    height: 105px;
    border-radius: 5px 0 0 5px;
    overflow: hidden;
  }
  .aside_right {
    width: 240px;
    // background: skyblue;
    line-height: 20px;
    margin-left: 10px;

    & > div {
      color: #333;
      font-size: 13px;
      margin: 5px 0 5px 0px;
      .icon {
        margin-right: 5px;
      }
    }
    & > div:nth-child(1) {
      margin-top: 0;
    }
    .head_title {
      & > span:nth-child(1) {
        font-size: 13px;
        display: inline-block;
        color: #fff;
        background-color: #00a0e9;
        border-radius: 5px 0 5px 0;
        padding: 0px 8px;
      }
      & > span:nth-child(2) {
        color: #333333;
        font-size: 15px;
        font-weight: bold;
        margin-left: 5px;
      }
    }
    .site {
      display: flex;
      // align-items: center;
      .icon {
        padding-top: 2px;
      }
    }
    .mode {
      display: flex;
      align-items: center;
    }
    .money_foot {
      display: flex;
      justify-content: space-between;
      align-items: center;
      & > div:nth-child(1) {
        // margin-left: -4px;
        & > span:nth-child(1) {
          margin-left: -8px;
        }
        .tag {
          color: #ffaa01;
          margin-right: 5px;
        }
      }
      & > div:nth-child(2) {
        color: #0bb754;
        font-size: 16px;
        font-weight: bold;
        small {
          font-size: 12px;
        }
      }
    }
  }
}
</style>