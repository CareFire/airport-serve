<template>
    <div>
        <img src="/static/images/houjidating.png" alt="">
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
        logs: []
      }
    },

    created () {

    }
  }
</script>

<style>
img {
    width: 96%;
    margin:0 2%;
}
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
