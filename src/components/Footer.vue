<template>
  <footer class="footer">
    <div class="message_title">
      活动须知
    </div>
    <div v-bind:class="{message_content:flag, message_content1:!flag}" id="messge_content">
      <p>1.本次活动有效期为：2016年2月6日至2016-2017赛季欧洲冠军联赛结束</p>
      <p>2.贴息率不固定，实际贴息以用户购买时的收益率计算为准</p>
      <p>3.在活动期间，投资活动项目，未全部猜对的用户，除本金外，将获得苏...</p>
      <p>4.在活动期间，投资活动项目，未全部猜对的用户，除本金外，将获得苏...</p>
      <p>5.在活动期间，投资活动项目，未全部猜对的用户，除本金外，将获得苏...</p>
    </div>
    <div class="message_b">
      <button id="add" v-on:click="addcc"  v-bind:class="{ bg1: flag, bg2:!flag}">{{flag?"展示全部":"合并"}}</button>
    </div>
  </footer>

</template>
<script>
export default {
  name: 'Footer',
  data () {
    return {
      flag: 1
    }
  },
  methods: {
    addcc: function () {
      this.flag = 1 - this.flag
    }
  }
}
</script>
<style>
  .footer{
    min-width: 320px;
    max-width: 750px;
    width: 100%;
    margin: 0 auto;
    margin-top: 5px;

  }
  .message_title{
    height: 44px;
    background: #fff;
    line-height: 46px;
    font-size: 15px;
    color: #489fe5;
    text-align: center;
  }

  .message_content{
    margin: 1px 0 1px 0;
    height: 74px;
    background: #fff;
    color: #666;
    padding: 15px 15px 30px 20px;
    border-bottom: 1px solid #ececec;
    overflow: hidden;
  }
  .message_content1{
    margin: 1px 0 1px 0;
    background: #fff;
    color: #666;
    padding: 15px 15px 15px 20px;
    border-bottom: 1px solid #ececec;
  }

  .message_content1 p,.message_content p{
    line-height: 20px;
    font-size: 12px;
  }
  .message_b{
    margin-top: 1px;
    height: 42px;
    background: #fff;
    text-align: center;
    position: relative;

  }

  .message_b .bg1{
    vertical-align: middle;
    position: absolute;
    background: url("../assets/mext_01.png")no-repeat;
    width: 80px;
    left: 50%;
    margin-left: -40px;
    margin-top: 15px;
    color: #909090;
    font-size: 12px;
    height: 12px;
    line-height: 12px;
    padding-left: 10px;
    text-decoration: none;
    border: none;
    outline: none;

  }.bg2{
       position: absolute;
       background: url("../assets/next_02.png")no-repeat;
       width: 80px;
       left: 50%;
       margin-left: -40px;
       margin-top: 15px;
       color: #909090;
       font-size: 12px;
       height: 12px;
       line-height: 12px;
       padding-left: 10px;
       text-decoration: none;
       border: 0;
       outline:none;
     }
</style>
