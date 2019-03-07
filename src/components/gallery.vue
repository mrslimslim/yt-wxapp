<template>
    <div class="gallery">
      <div class="title">
        {{titleText}}
      </div>
      <div class="content">
        <div class="box" v-for="(item, index) in galleryArrs" :key="index">
            <div class="thumb">

            </div>
            <div class="desc">

            </div>
            
      </div>
      </div>
      
    </div>
    
</template>

<script>
export default {
  props: ['galleryArrs'],
  data () {
    return {
      titleText: '咖啡+祝福 即刻表心意'
    }
  }
}
</script>

<style scoped>
   .gallery{
       padding: 0 36rpx;
   }
  .title{
      font-size: 24rpx;
      margin-bottom: 24rpx;
  }
  .content{
      display: flex;
      width: 100%;
      flex-wrap: wrap;
      justify-content: space-between;
  }
  .box{
      width: 320rpx;
      height: 240rpx;
      background:pink;
      margin-bottom: 24rpx;
  }
</style>
