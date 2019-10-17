<template>
  <div class="wrapper">
    <div id="active-card-div" style="background-image: url('/static/images/vipcard.png');">
      <p @click="onRoute()">点击激活会员卡</p>
    </div>
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
    }
  },
  components: {
    card
  },
  methods: {
    onRoute () {
      wx.navigateTo({ url: '/pages/detail/main' })
    }
  },
  created () {

  }
}
</script>

<style scoped>
.wrapper {
  padding: 20rpx;
}

.gray {
  -webkit-filter: grayscale(100%);
  -moz-filter: grayscale(100%);
  -ms-filter: grayscale(100%);
  -o-filter: grayscale(100%);
  filter: grayscale(100%);
  filter: gray;
}

#active-card-div {
  width:100%;
  height:400rpx;
  text-align:center;
  background-size: 100%;
  background-repeat: no-repeat;
}

#active-card-div p {
  line-height: 400rpx;
}

#notice-div {
  width: 100%;
}

.notice-middle-div {
  width:48%;
  margin:0 1%;
  float: left;
  text-align: center;
  box-sizing: border-box;
  border: 1rpx solid #ddd;
  border-radius: 5%;
}
</style>
