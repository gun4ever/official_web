<template>
  <div class="footer" v-show="isShow">
    <!-- <a target="_blank" href="http://wpa.qq.com/msgrd?v=3&uin=3080727502&site=qq&menu=yes"><img border="0" src="http://wpa.qq.com/pa?p=2:3080727502:52" alt="点击这里给我发消息" title="点击这里给我发消息"/></a> -->
    <div class="footer-wrap">
      <div class="gongzhong">
        <img src="./image/code.png" alt="">
        <div class="guanzhu">关注微信号</div>
      </div>
      <div class="detail-info">
        <ul>
          <li class="phone-content">
            <img src="./image/d_call.png" alt="">
            <div class="phone-wrap">
              <div class="phone-text">全国服务热线</div>
              <div class="phone">028-8231-2656</div>  
            </div>
          </li>
          <li class="o-info">地址：四川省崇州市崇阳街道向荣街361号附301-303号3层</li>
          <li class="o-info">Copyright &copy 2018 大划建筑版权所有</li>
          <li class="o-info">蜀ICP备18003830号</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        isShow:false    
      }
      
    },
    watch:{
      $route(to,from){
        this.isShow = false
        setTimeout(() => {
          this.isShow = true
        },200)
      }
    },

    
  }
</script>

<style scoped lang="less" rel="stylesheet/less">
  @import "~common/less/variable.less";

  .footer {
    position: relative;
    z-index: 100;
    min-width:1200px;
    height:200px;
    background:#1d2026;
    .footer-wrap {
      position: fixed;
      left:0;
      bottom:0;
      height:200px;
      width:960px;
      margin:0 auto;
      position:relative;
      overflow:hidden;
      .gongzhong {
        position:absolute;
        top:44px;
        left:0;
        img {
          vertical-align:middle;
          width:110px;
          height:110px;
          display:inline-block;
        }
        .guanzhu {
          color:#cfcfcf;
          position:absolute;
          top:18px;
          left:120px;
          display:inline-block;
          width:15px;
          height:110px;
        }
      }
      .detail-info {
        color:#fff;
        text-align:center;
        .phone-content {
          margin-top:39px;
          margin-bottom:30px;
          .phone-wrap {
            display:inline-block;
            .phone-text {
              font-size:14px;
              text-align:left;
            }
            .phone {
              margin-top:5px;
              font-size:36px;
            }
          }
        }
        .o-info {
          font-size:14px;
          color:#b9b9b9;
          margin-top:10px;
        }
      }
    }
  }
</style>
