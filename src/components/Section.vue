<template>
  <section class="list clear">
      <ul>
        <li>
          <p class="title">猜冠军</p>
          <p class="numb"><span>+79.5</span></p>
          <p class="content1">最高年化收益</p>
          <p class="day1">120天&nbsp;1000元起</p>
          <div class="btn">
            <span href="javascript:void(0);">我要抢</span>
          </div>
        </li>
        <li>
          <p class="title">猜最佳射手</p>
          <p class="numb"><span>+37.5</span></p>
          <p class="content1">最高年化收益</p>
          <p class="day1">120天&nbsp;1000元起</p>
          <div class="btn">
            <span href="javascript:void(0);">我要抢</span>
          </div>
        </li>
        <li>
          <p class="title">猜八强</p>
          <p class="numb"><span>+135.8</span></p>
          <p class="content1">最高年化收益</p>
          <p class="day1">120天&nbsp;1000元起</p>
          <div class="btn">
            <span href="javascript:void(0);">我要抢</span>
          </div>
        </li>
        <li>
          <p class="title">猜胜平负{{flag}}</p>
          <p class="numb"><span>+158.2</span></p>
          <p class="content1">最高年化收益</p>
          <p class="day1">120天&nbsp;1000元起</p>
          <div class="btn">
            <span href="javascript:void(0);">我要抢</span>
            <router-link :to="{ name: 'AbHeader' }">AbHeader</router-link>
          </div>
        </li>
      </ul>
  </section>
</template>
<script>
export default {
  name: 'Header',
  data () {
    return {
      flag: ''
    }
  },
  mounted: function () {
    this.$bus.on('msg', (e) => {
      this.flag = e
    })
  }
}
</script>
<style>
  .list{
    width: 100%;
    min-width: 320px;
    max-width: 750px;
    margin: 0px auto;
    text-align: center;
  }
  .list li{
    width: 48%;
    background: #fff;
    margin-top: 5px;
  }
  .list li:nth-child(odd){
    float:left;
    margin-left: 1.3%;
  }
  .list li:nth-child(even){
    float: right;
    margin-right: 1.3%;
  }

  .list p{
    text-align: center;
  }
  .list .title{
    font-size: 17px;
    padding-top: 8%;
    color: #394148;
    height: 32px;
    line-height: 32px;
    font-weight: 700;

  }
  .list .numb{
    color: #f7941e;
    margin-top: 5px;
    height: 30px;
    line-height: 30px;

  }
  .numb span{
    font-size: 29px;
  }
  .numb span:after{
    font-size: 15px;
    content: "%";
  }
  .list .content1{

    color: #666;
    font-size: 11px;
    height: 12px;
    line-height: 12px;
    margin-top: 5px;
  }
  .list .day1{
    margin-top: 9px;
    color:#909090;
    height: 24px;
    line-height: 24px;
    font-size: 12px;
    margin-bottom: 10px;
  }

  .btn{
    width: 50%;
    background: #f7941e;
    color: #fff;
    font-size: 15px;
    border-radius:4px;
    text-align: center;
    left: 23%;
    position: relative;
    margin-bottom: 18px;
    padding: 6px 6px;
  }
  .btn a {
    display: block;
    color: #fff;
    height:100%;
  }
  .btn a,.btn a:hover{
    text-decoration: none;
    outline: none;
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
