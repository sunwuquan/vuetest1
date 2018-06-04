<template>
  <div>
    <header class="clear header">
      <a href="#"><img src="../assets/back.gif" alt="返回"></a>
      <h1>欧冠竞猜理财</h1>
    </header>
    <div class="pic">
      <img src="../assets/pic.png" alt="标题">
    </div>
    <div class="plan">
      <div class="plan_top">
        <div class="plan_top_title">
          <span class="p_line"></span>
          <img src="../assets/rmb.png" alt="">
          <span v-on:click="clickMe">理财方案</span>
          <span class="p_line"></span>
        </div>
      </div>
      <p class="text1 clear">方案均为懂球帝&苏宁金融合作出品</p>
      <p class="text2"><span>{{flag}}{{message}}</span>保底年化收益</p>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Header',
  data () {
    return {
      flag: 0
    }
  },
  props: {
    message: ''
  },
  methods: {
    addcc: function () {
      this.flag = 1 - this.flag
      console.log('addcc')
    },
    clickMe: function () {
      this.$bus.emit('msg', '传递的值')
    }
  },
  created: function () {
    // `this` 指向 vm 实例
    this.flag = 9
    let that = this
    console.log('a is: ' + this.flag)
    this.$ajax({
      method: 'get',
      url: 'http://localhost:8081/#/',
      data: {
        name: 'haha'
      }
    }).then(function (res) {
      console.log(res)
      that.addcc()
      that.flag = 100
    }).catch(function (err) {
      console.log(err)
    })
  }
}
</script>

<style>
  .header{
    margin: 0 auto;
    min-width: 320px;
    max-width: 750px;
    height: 3rem;
    width: 100%;
    background: #00ae32;
    border-bottom: 1px solid #009c2d;
    text-align: center;
  }
  .header a {
    float: left;
    border: 1px solid #00ae32;
    width: 22px;
    height: 18px;
    position: relative;
    margin-left: 1.5rem;
    /*padding-top: 0.9rem;*/
    display: block;
    top:50%;
    transform: translateY(-50%);
  }
  .header a img{
    height: 18px;
    width: 22px;
    display: inline-block;
  }
  .header h1{
    color: #fff;
    position: relative;
    /*left: 50%;*/
    /*width: 12.5rem;*/
    /*width: 200px;*/
    font-size: 17px;
    /*margin-left: -90px;*/
    /*top: 1rem;*/
    top:50%;
    transform: translateY(-50%);
    /*padding-top: 8px;*/
  }
  .pic{
    width: 100%;
    min-width: 320px;
    max-width: 750px;
    margin: 0 auto;
  }
  .pic img{
    width: 100%;
    display: block;
  }
  .plan{
    min-width: 320px;
    max-width: 750px;
    background: #ffffff;
    width: 100%;
    margin: 0 auto;
  }
  .plan_top{
    width:100%;
    padding-top: 15px;
    height: 17px;
    line-height: 34px;
    padding-bottom: 10px;
  }
  .plan_top_title{
    text-align: center;
    color: #1790e2;
    font-weight: 700;
    font-size: 15px;
    vertical-align: middle;
  }
  .p_line{
    height: 1px;
    width: 44px;
    background:#1790e2;
  }
  .plan_top_title img{
    width: 17px;
    height: 17px;
    vertical-align: middle;
    margin-left: 5px;
  }
  .plan_top_title span{
    display: inline-block;
    vertical-align: middle;
    margin-right: 5px;
  }
  .plan_top img{
    height: 17px;
    width: 17px;
  }
  .plan .text1{
    text-align: center;
    color: #909090;
    font-size: 13px;
    line-height: 16px;
    margin-top: 5px;
  }
  .text2{
    color: #909090;
    font-size: 13px;
    line-height: 26px;
    text-align: center;
    padding-bottom: 10px;
  }
  .text2 span{
    color: #f7941e;
    margin-right: 10px;
  }
  .clear{
    zoom: 1;
  }
  .clear:after{
    content: '';
    display: block;
    clear: both;
  }
</style>
