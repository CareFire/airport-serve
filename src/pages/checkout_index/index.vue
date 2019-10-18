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
    img {
        width: 100%;
        height:350rpx
    }
    .indexContainer swiper {
        width: 100%;
        height:400rpx;
    }

    .indexContainer swiper img {
        width:100%;
        height:100%;
    }
</style>
