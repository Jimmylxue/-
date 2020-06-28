<template>
  <div class="order alluse">
    <van-nav-bar
      title="订单"
      left-text=""
      right-text=""
      left-arrow
      @click-left="onClickLeft"
    />
    <van-search
      v-model="value"
      background="#F3F3F3"
      placeholder="请输入搜索关键词"
    />
    <items></items>
    <items></items>
    <items></items>
  </div>
</template>

<script>
import items from '@/components/page/hotel/components/orderitem.vue'
export default {
  components:{
    // claps
    items
  },
  methods: {
    onClickLeft(){}
  },
}
</script>

<style lang="less" scoped>
.order{
  width: 100%;
  height: 100vh;
  background-color: rgba(243,243,243,1);
  font-size: 14px;
  overflow: auto;
}
// .items{
//   padding: 5px 10px 10px 10px;
//   background-color: #fff;
//   &>div:nth-child(1){
//     display: flex;
//     justify-content: space-between;
//     border-bottom: 1px solid rgb(243, 243, 243);
//     padding-bottom: 5px;
//   }
//   &>div:nth-child(2){
//     width: 100%;
//     display: flex;
//     align-items: center;
//     border-bottom: 1px solid rgb(243, 243, 243);
//     margin: 5px 0;
//     padding-bottom: 5px;
//     &>div:nth-child(1){
//       width:29%;
//       height: 105px;
//       // margin-right: 10px;
//     }
//     &>div:nth-child(2){
//       width: 71%;
//       padding-left: 10px;
//       display: flex;
//       flex-direction: column;
//       height: 105px;
//       justify-content: space-between;
//       &>div:nth-child(1){
//         color: #333333;
//         font-weight: bold;
//         line-height: 20px;
//       }
//       &>div:nth-child(2){
//         color: rgb(161, 161, 161);
//         font-size: 12px;
//         p{
//           margin-top: -5px;
          
//         }
//         &>p:nth-child(1){
//           margin-bottom: 5px;
//         }
//       }
//     }
//   }
//   &>div:nth-child(3){
//     display: flex;
//     flex-direction: column;
//     align-items: flex-end;
//     p{
//       color: rgb(34, 34, 34);
//       span{
//         font-size: 18px;
//         margin-left: 2px;
//       }
//     }
//     button{
//       width: 75px;
//       height: 25px;
//       color: rgb(100, 100, 100);
//       border: 1px solid rgb(209, 209, 209);
//       border-radius: 20px;
//       background-color: #fff;
//       display: flex;
//       justify-content: center;
//       align-items: center;
//       // padding-bottom: 20px;
//     }
//   }
// }
</style>