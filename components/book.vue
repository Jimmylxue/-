<template>
  <div class="book alluse">
    <van-nav-bar title="标题" left-text left-arrow @click-left="onClickLeft">
      <template #title>
        <div class="book_title">
          <span :class="isCheck===1?'isactive':''" @click="isCheck=1">预定同住</span>
          <span :class="isCheck===2?'isactive':''" @click="isCheck=2">已定同住</span>
        </div>
      </template>
    </van-nav-bar>
    <div class="book_toggle">
      <div class="tab">
        <div>推荐地区</div>
        <div>
          位置排序
          <van-icon class="icons" name="arrow-up" />
        </div>
        <div>
          价格排序
          <van-icon class="icons" name="arrow-up" />
        </div>
        <div>
          好评优先
          <van-icon class="icons" name="arrow-up" />
        </div>
      </div>
      <togger></togger>
      <togger></togger>
      <togger></togger>
    </div>
  </div>
</template>

<script>
import togger from "@/components/page/hotel/components/togger.vue";
export default {
  components: {
    togger
  },
  data() {
    return {
      isCheck: 1
    };
  },
  methods: {
    onClickLeft() {
      this.$router.go(-1);
    }
  }
};
</script>

<style lang="less" scoped>
.book {
  font-size: 14px;
}
.book_title {
  span {
    margin: 0 5px;
  }
  .isactive {
    font-size: 16px;
    font-weight: bold;
    color: #000;
  }
}

.tab {
  width: 100%;
  height: 40px;
  display: flex;
  // background-color: skyblue;
  align-items: center;
  font-size: 12px;
  div {
    // flex-grow: 1;
    width: 25%;
    display: flex;
    height: 20px;
    justify-content: center;
    align-items: center;
    color: #333333;
    border-right: 1px solid #b5b5b5;
    line-height: 20px;
    .icons {
      margin-left: 2px;
      padding-bottom: 2px;
    }
  }
  & > div:nth-child(4) {
    border-right: none;
  }
}
</style>