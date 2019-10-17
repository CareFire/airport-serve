<template>
    <div>
        <swiper v-if="imgUrls.length > 0" indidator-dots="imgUrls.length > 1" >
            <block v-for="(item, index) in imgUrls" :key="index" >
                <swiper-item>
                    <image :src="item" mode="scaleToFill"></image>
                </swiper-item>
            </block>
        </swiper>
        <div class="choice-div">
            <div class="div-inline">
                <p>1元</p>
                <p>4次</p>
            </div>
            <div class="div-inline">
                <p>1元</p>
                <p>4次</p>
            </div>
            <div class="div-inline">
                <p>1元</p>
                <p>4次</p>
            </div>
            <div class="div-inline">
                <p>1元</p>
                <p>4次</p>
            </div>
            <div class="div-inline">
                <p>1元</p>
                <p>4次</p>
            </div>
            <div class="div-inline">
                <p>1元</p>
                <p>4次</p>
            </div>
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
        logs: [],
        imgUrls: [
          '/static/images/houjidating.png'
        ]
      }
    },

    created () {

    }
  }
</script>

<style>
.choice-div {
    width: 100%;
    height:140rpx;
}
.div-inline{
    width:25%;
    height: 140rpx;
    float: left;
    margin: 10rpx 4.16%;
    box-sizing: border-box;
    border:1rpx solid black;
    border-radius: 10rpx;
}

.div-inline p {
    text-align: center;
    line-height: 70rpx;
}
</style>
