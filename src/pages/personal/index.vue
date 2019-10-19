<template>
  <div class="indexContainer">
    <div class="userinfo" style="background-image: url('/static/images/personal-bgimg.jpeg')" v-if="userInfo.nickName">
      <img class="userinfo-avatar" :src="userInfo.avatarUrl"/>
      <span class="name-span">{{userInfo.nickName}}</span>
      <span class="user-type-span">个人用户</span>
    </div>
    <div class="user-info-detail">
      <div>
        <p>剩余次数</p>
        <p>100</p>
      </div>
      <div class="used-num-div">
        <p>已用次数</p>
        <p>0</p>
      </div>
      <div>
        <p>积分</p>
        <p>0</p>
      </div>
    </div>
    <ul class="menu-ul">
      <li> 我的订单</li>
      <li> VIP贵宾次数卡</li>
    </ul>
  </div>
</template>

<script>
import card from '@/components/card'

export default {
  components: {
    card
  },

  data () {
    return {
      userInfo: {}
    }
  },
  methods: {
    getUserInfo () {
      var _this = this
      wx.getStorage({
        key: 'user_info',
        success: function (r) {
          console.log(11122233)
          console.log(r.data)
          _this.userInfo = r.data
        },
        fail: function () {
          console.log('读取user_key发生错误')
        }
      })
    }
  },
  created () {
    this.getUserInfo()
  }
}
</script>

<style>
  page {
    background: #ffffff;
  }
  .indexContainer {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .userinfo-avatar {
    width:100rpx;
    height: 100rpx;
    position:absolute;
    left:30rpx;
    top:30rpx;
    border-radius:50%;
  }
  .userinfo {
    width: 96%;
    margin:0 auto;
    height:200rpx;
    background-size: 100% 100%;
    background-repeat: no-repeat;
  }

  .userinfo .name-span {
    position: absolute;
    left: 145rpx;
    top: 45rpx;
    font-size: 30rpx;
    color: black;
  }

  .userinfo .user-type-span {
    position: absolute;
    left: 145rpx;
    top: 75rpx;
    font-size: 30rpx;
    color: black;
  }

  #active-card-div p {
    line-height: 400rpx;
  }

  .user-info-detail {
    width: 96%;
    margin: 0 auto;
    height: 120rpx;
    background: pink;
  }
  .user-info-detail div {
    width: 30%;
    height:100%;
    float: left;
    margin: 0 auto;
    background: yellow;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .used-num-div {
    margin: 0 5% !important;
  }

  .menu-ul {
    width: 96%;
    margin: 0 auto;
  }

  .menu-ul li {
    width: 100%;
    height:70rpx;
    line-height: 70rpx;
    text-align: left;
    background: #ddd;
    margin: 10rpx auto;
  }
</style>
