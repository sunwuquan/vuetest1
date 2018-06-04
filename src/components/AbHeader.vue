<template>
  <header class="header">
    <div class="title">
      <a href="javascript:void(0);"><img src="../assets/back.gif" alt="返回键"></a>
      <h1>欧冠八强竞猜理财</h1>
    </div>
    <div class="pic">
      <img src="../assets/ab_pic.png" alt="">
      <div class="pic_btn">
        <div class="pic_btn_left">
          <p>保底年化收益</p>
          <p class="pic_numbSize"><span id="year">4</span></p>
        </div>
        <div class="pic_btn_cen">
          <p class="pic_btn_cen_title">猜对懂球帝加将:</p>
          <p class="pic_numbSize" id="award"><span>2.0</span>~<span>135.8</span></p>
        </div>
        <div class="pic_btn_right">
          <p class="pic_btn_right_text">起投金额(元):</p>
          <p class="pic_numbSize" id="money">1000</p>
        </div>
      </div>
    </div>
  </header>
</template>
<script>
export default {
  name: 'AbHeader',
  data () {
    return {
      flag: 1
    }
  }
}</script>
<style>
  .header{
    min-width: 320px;
    max-width: 750px;
    margin: 0 auto;
  }
  .title{
    width: 100%;
    margin: 0 auto;
    text-align: center;
    background: #00ae32;
    border-bottom: 1px solid #009c2d;
    height:40px;
  }
  .title a{
    margin-top: 12px;
    margin-left: 10px;
  }
  .title a,.title a img{
    display:inline-block;
    width: 22px;
    height: 18px;
    float: left;
  }
  .title h1{
    display: inline-block;
    line-height: 40px;
    color: #fff;
  }
  /*头部结束*/

  /*图片展示区开始*/
  .pic{
    position: relative;
    width: 100%;
  }
  .pic img{
    width: 100%;
    display: block;
  }
  .pic_btn{
    position: absolute;
    width: 100%;
    height: 24%;
    background: rgba(19,29,11,0.9);
    bottom: 0%;
  }
  .pic_btn_left{
    width: 30%;
    float: left;
    height: 100%;
    color: #babbb9;
    text-align: center;
    padding-top: 6px;
  }
  .pic_numbSize{
    font-size: 20px;
    padding-top: 3px;
  }
  .pic_numbSize span:after{
    content: "%";
    font-size: 10px;
  }
  .pic_btn_cen{
    float: left;
    text-align: center;
    width: 40%;
    color: #fff;
    padding-top: 6px;
  }
  .pic_btn_cen_title{
    font-size: 10px;
  }
  .pic_btn_right{
    float: right;
    width: 30%;
    height: 100%;
    text-align: center;
    padding-top: 6px;
    color: #b9babc;
  }
  .pic_btn_right_text{
    font-size: 10px;
    color: #b9babc;
  }
</style>
