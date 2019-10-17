<template>
  <div class="wrapper">
    <image class="head-image gray" src="/static/images/vipcard.png"/>
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
  },
  created () {

  }
}
</script>

<style scoped>
.wrapper {
  padding: 20rpx;
}
.head-image {
  width:100%;
  height: 400rpx;
  border-radius:3%;
}
.gray {
  -webkit-filter: grayscale(100%);
  -moz-filter: grayscale(100%);
  -ms-filter: grayscale(100%);
  -o-filter: grayscale(100%);
  filter: grayscale(100%);
  filter: gray;
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
