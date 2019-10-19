<template>
  <div class="indexContainer">
    <div class="userinfo" v-if="userInfo.nickName">
      <img class="userinfo-avatar" :src="userInfo.avatarUrl"/>
      <span>{{userInfo.nickName}}</span>
    </div>
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

  .userinfo span {
    position: absolute;
    left: 145rpx;
    top: 45rpx;
    font-size: 30rpx;
    color: black;
  }

  #active-card-div p {
    line-height: 400rpx;
  }
</style>
