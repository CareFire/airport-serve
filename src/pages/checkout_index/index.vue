<template>
    <div class="indexContainer">
        <swiper indicator-dots indicator-color="white" indicator-active-color="green">
            <swiper-item>
                <img src="/static/images/houjidating.png" alt="">
            </swiper-item>
            <swiper-item>
                <img src="/static/images/vipcard.png" alt="">
            </swiper-item>
        </swiper>
        <div class="notice-div">
            <div class="notice-middle-div">
                <img src="/static/images/checkout-logs.png" alt="">
            </div>
            <div class="notice-middle-div">
                <img src="/static/images/scan-checkout.png" alt="">
            </div>
        </div>
        <p class="little-title">近期核销记录</p>
        <div class="recent-logs">
            <div class="logo">
                <img class="logo-img" src="/static/images/logo.jpeg" alt="">
            </div>
            <p><span>小明</span><span>2019-10-01 00:00:00</span>核销成功！</p>
            <p><span>小明</span><span>2019-10-01 00:00:00</span>核销成功！</p>
            <p><span>小明</span><span>2019-10-01 00:00:00</span>核销成功！</p>
            <p><span>小明</span><span>2019-10-01 00:00:00</span>核销成功！</p>
            <p><span>小明</span><span>2019-10-01 00:00:00</span>核销成功！</p>
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

<style>
    page {
        background: #ffffff;
    }

    .indexContainer swiper {
        width: 100%;
        height:400rpx;
    }

    .indexContainer swiper img {
        width:100%;
    }
    .notice-div {
        width: 96%;
        margin: 10rpx auto;
    }

    .notice-middle-div {
        width:48%;
        margin:0 1%;
        float: left;
    }

    .notice-middle-div img {
        width:100%;
        height:200rpx;
    }

    .little-title {
        width: 96%;
        margin: 0 2%;
    }

    .recent-logs {
        width: 96%;
        height:500rpx;
        margin: 0 2%;
        border-radius: 10rpx;
        background: #ddd;
    }

    .logo-img {
        width: 100rpx;
        height: 100rpx;
        border-radius: 50%;
        margin: 10rpx;
    }

    .recent-logs p {
        text-align: center;
    }
</style>
