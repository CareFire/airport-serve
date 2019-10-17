<template>
  <div class="wrapper">
    <image class="head-image gray" src="/static/images/vipcard.png"/>
    <van-button type="primary">主要按钮</van-button>
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
}
.gray {
  -webkit-filter: grayscale(100%);
  -moz-filter: grayscale(100%);
  -ms-filter: grayscale(100%);
  -o-filter: grayscale(100%);
  filter: grayscale(100%);
  filter: gray;
}
</style>
