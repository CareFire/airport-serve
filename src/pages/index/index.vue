<template>
  <div class="indexContainer">
    <div id="active-card-div" style="background-image: url('/static/images/vipcard.png');">
      <div class="userinfo" v-if="userInfo.nickName">
        <img class="userinfo-avatar" :src="userInfo.avatarUrl"/>
        <span>{{userInfo.nickName}}</span>
      </div>
      <p @click="onRoute()">点击激活会员卡</p>
    </div>
    <button v-if="!userInfo.nickName" open-type="getUserInfo" @getuserinfo="authSetUser">
      授权登录
    </button>
    <div id="notice-div">
      <div class="notice-middle-div">
        <p>剩余次数</p>
        <p>0</p>
      </div>
      <div class="notice-middle-div">
        <p>已用次数</p>
        <p>0</p>
      </div>
    </div>
  </div>
</template>

<script>
import card from '@/components/card'

export default {
  data () {
    return {
      userInfo: {}
    }
  },
  components: {
    card
  },
  methods: {
    onRoute () {
      wx.navigateTo({ url: '/pages/checkout_index/main' })
    },
    authSetUser (e) {
      this.userInfo = e.mp.detail.userInfo
    },
    getUserInfo () {
      // 调用登录接口
      var _this = this
      wx.getUserInfo({
        success (res) {
          console.log(res)
          _this.userInfo = res.userInfo
        },
        fail (err) {
          console.log(err)
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

.userinfo span {
  position: absolute;
  left: 145rpx;
  top: 45rpx;
  font-size: 30rpx;
  color: white;
}
#active-card-div {
  width:96%;
  height:400rpx;
  margin:10rpx auto;
  border-radius: 10rpx;
  text-align:center;
  background-size: 100%;
  background-repeat: no-repeat;
}

#active-card-div p {
  line-height: 400rpx;
}

#notice-div {
  width: 96%;
}

.notice-middle-div {
  width:48%;
  margin:0 1%;
  float: left;
  text-align: center;
  box-sizing: border-box;
  border: 5rpx solid #ddd;
  border-radius: 10rpx;
}
</style>
