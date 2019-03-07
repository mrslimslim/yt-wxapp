<template>
  <div class="parent">
    <swiper class="swiper" :circular='circular' :indicator-color='indicatorColor' :indicator-active-color='indicatorActiveColor' :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
        <block v-for="(item, index) in images" :key="index">
            <swiper-item>
                <image :src="item.url" class="slide-image" mode="aspectFill"/>
            </swiper-item>
        </block>
    </swiper> 
  </div>
</template>

<script>

import { DOT_COLOR, DOT_ACTIVE_COLOR } from '@/constants'

export default {
  props: ['images'],
  data () {
    return {
      indicatorDots: true,
      autoplay: true,
      circular: true,
      interval: 3000,
      duration: 500,
      indicatorColor: DOT_COLOR,
      indicatorActiveColor: DOT_ACTIVE_COLOR
    }
  }
}
</script>

<style>
.parent{
  width: 100%;
}
.swiper {
  height: 600rpx;
}
image {
  width: 100%;
  height: 600rpx;
}
</style>
