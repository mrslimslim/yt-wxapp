<template>
    <div class="history">
        <div class="icon">

        </div>
        <div class="link">
            <a href="/">{{buyText}}</a>
        </div>
    </div>
</template>

<script>
export default {
  data () {
    return {
      buyText: '购买历史'
    }
  }
}
</script>

<style>
    .history{
        width: 100%;
    }
    .icon{
        width: 60rpx;
        height: 60rpx;
        margin: 0 auto;
        background: skyblue;
        border-radius: 50%;
        box-shadow: 0 5px 5px #c5c5c5;
        margin-bottom: 16rpx;
    }
    .link{
        width: 100%;
        text-align: center;
        height: 60rpx;
        font-size: 22rpx;
        color: green;
    }
</style>
