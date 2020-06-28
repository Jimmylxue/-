<template>
  <div class="camera alluse">
    <van-nav-bar
      title="随手拍"
      left-text=""
      right-text=""
      left-arrow
      @click-left="onClickLeft"
    />
    <div class="text">
      <textarea cols="30" placeholder="您可以再这里输入内容，记录酒店的一切" rows="10"></textarea>
    </div>
    <div class="heada">
      <span>图片上传</span><span>您最多可以上传6张图片</span>
    </div>
    <div class="imgform">
      <van-uploader preview-size="110px" v-model="fileList" multiple :max-count="6" />
    </div>
    <span class="locoala">
      <van-icon name="location-o" />如家福州金融街万达广场店
    </span>
    <div class="footbar">提交审核</div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      fileList: [],
    }
  },
  methods: {
    onClickLeft(){}
  }
}
</script>

<style lang="less" scoped>
.camera{
  font-size: 14px;
  height: 100vh;
  background-color: rgba(248,248,248,1);
}
.text{
  width: 100%;
  margin-top: 10px;
  // padding: 5px 10px 0px 10px;
  textarea{
    width: 100%;
    height: 130px;
    padding: 10px;
    border: none;
    border-bottom: 1px solid rgba(238,238,238,1);
    resize: none;  //禁止调整宽高
  }
}
.heada{
  padding: 0px 10px;
  width: 100%;
  background-color: #fff;
  padding-top: 5px;
  // height: 35px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  &>span:nth-child(1){
    color: #3A4658;
  }
  &>span:nth-child(2){
    color: #48576C;
    height: 20px;
    font-size: 12px;
    display: inline-block;
    background-color: rgba(236,236,236,1);
    padding: 0 5px;
  }
}
.imgform{
  padding: 5px 10px;
  display: flex;
  justify-content: space-between;
  margin-bottom: 10px;
  background-color: #fff;
}
.locoala{
  background-color: rgba(255,213,0,.2);
  color: #333333;
  // width: 200px;
  // display: flex;
  align-items: center;
  line-height: 20px;
  padding: 2px 5px;
  // margin-top: 10px;
  margin-left: 10px;
  // line-height: 25px;
}
.footbar{
  width: 100%;
  height: 50px;
  background-color: #00A0E9;
  color: #fff;
  font-size: 18px;
  display: flex;
  justify-content: center;
  align-items: center;
  font-weight: bold;
  position: fixed;
  bottom: 0;
}
</style>