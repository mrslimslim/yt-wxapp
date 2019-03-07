<template>
    <div class="bonus">
        <div class="coupon"></div>
        <div class="collect">
            <span class="word">{{collectText}}</span>
            <div class="collect-btn">
            </div>
        </div>
    </div>
</template>

<script>
export default {
  props: ['images'],
  data () {
    return {
      collectText: '收藏'
    }
  }
}
</script>

<style>
    .bonus {
        display: flex;
        width: 100%;
        height: 120rpx;
        align-items: center;
        justify-content: space-around;
    }
    .coupon {
        width: 300rpx;
        height: 60rpx;
        border-radius: 30rpx;
        box-shadow: 0 0 5px #c5c5c5;
    }
    .collect {
        width: 160rpx;
        height: 60rpx;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .word {
        font-size: 22rpx;
        color: green;
    }
    .collect-btn{
        background: pink;
        width: 60rpx;
        height: 60rpx;
        border-radius: 50%;
    }
</style>
