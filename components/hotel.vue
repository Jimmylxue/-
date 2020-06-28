<template>
  <div class="hotel">
    <button @click="$router.push('/page/listpage')">列表页</button>
    <button @click="$router.push('/page/detail')">详情页</button>
    <button @click="$router.push('/page/reserve')">预定</button>
    <button @click="$router.push('/page/clap')">随手拍列表</button>
    <button @click="$router.push('/page/order')">酒店订单</button>
    <button @click="$router.push('/page/orderdetail')">订单详情</button>
    <button @click="$router.push('/page/camera')">随手拍发布</button>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="less" scoped>
.hotel{
  font-size: 14px;
}
</style>