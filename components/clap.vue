<template>
  <div class="clap">
    <nav>
      <van-nav-bar
        title="标题"
        left-text=""
        right-text=""
        left-arrow
        @click-left="onClickLeft"
        @click-right="onClickRight"
      >
        <template #left>
            <div style="display:flex;align-items: center; transform:">
              <van-icon class="back" name="arrow-left" />
            </div>
          </template>
        <template #title>
          <div class="title">
            <span :class="titleSelect===1?'iselect':''" @click="titleSelect = 1">随手拍</span>
            <span :class="titleSelect===2?'iselect':''" @click="titleSelect = 2">我的</span>
          </div>
        </template>
        <template #right>
          <div class="toclap">
            <van-icon class="icons" name="video-o" />拍一个
          </div>
        </template>
      </van-nav-bar>
    </nav>
    <claps></claps>
    <claps></claps>
  </div>
</template>

<script>
import claps from '@/components/page/hotel/components/claps.vue'
export default {
  components:{
    claps,
  },
  data() {
    return {
      titleSelect:1
    }
  },
}
</script>

<style lang="less" scoped>
.clap{
  font-size: 14px;
  height: 100%;
  overflow: auto;
  background-color: rgba(248,248,248,1);
}
.title{
  span{
    margin: 0 5px;
  }
}
.iselect{
  font-size: 16px;
  // color: red;
  font-weight: bold;
}
.back{
  color: #B5B5B5;
  transform: scale(1.5);
}
.toclap{
  display: flex;
  width: 75px;
  height: 20px;
  background:rgba(0,160,233,1);
  opacity:1;
  border-radius:5px 0px 5px 0px;
  color: #fff;
  justify-content: center;
  align-items: center;
  font-size: 13px;
  .icons{
    color: #fff;
    margin-right: 3px;
    transform: scale(1.2);
  }
}

.amsg{
  width: 100%;
  // height: 540px;
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
    display: grid;
    width: 100%;
    height: 200px;
    height: 230px;
    grid-gap: 8px;
    grid-template-rows: repeat(2,1fr);
    grid-template-columns: repeat(3,1fr);
    div{
      width: 100%;
      height: 100%;
      background: sienna;
    }
  }
  .do{
    display: flex;
    justify-content: space-between;
    margin-top: 10px;
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