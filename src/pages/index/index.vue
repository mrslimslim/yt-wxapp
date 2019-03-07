<template>
  <div @click="clickHandle">
    <div class="swiper">
      <swiperHeader :images='imgArrs' ></swiperHeader>
    </div>
    <div class="bouns">
      <bonus></bonus>
    </div>
    <div class="gallery">
      <gallery :galleryArrs='galleryArrs'></gallery>
    </div>
    <div class="history">
      <buyHistory></buyHistory>
    </div>
    
  </div>
</template>

<script>
import card from '@/components/card'
import swiperHeader from '@/components/swiper-header'
import bonus from '@/components/bonus'
import gallery from '@/components/gallery'
import buyHistory from '@/components/buy-history'

export default {
  data () {
    return {
      imgArrs: [{
        url: '/static/images/starbucks1.jpeg'
      },
      {
        url: '/static/images/starbucks1.jpeg'
      },
      {
        url: '/static/images/starbucks1.jpeg'
      }
      ],
      galleryArrs: [{
        url: '/static/images/starbucks1.jpeg',
        description: '沉醉花花世界'
      },
      {
        url: '/static/images/starbucks1.jpeg',
        description: '定制星意祝福'
      },
      {
        url: '../../../static/images/starbucks1.jpeg',
        description: '只想粘着你'
      },
      {
        url: '../../../static/images/starbucks1.jpeg',
        description: '有你真好'
      },
      {
        url: '../../../static/images/starbucks1.jpeg',
        description: '咖啡有你'
      },
      {
        url: '../../../static/images/starbucks1.jpeg',
        description: '可爱第一名'
      },
      {
        url: '../../../static/images/starbucks1.jpeg',
        description: '为你加油'
      },
      {
        url: '../../../static/images/starbucks1.jpeg',
        description: '生日快乐'
      }
      ]
    }
  },

  components: {
    card,
    swiperHeader,
    bonus,
    gallery,
    buyHistory
  },

  methods: {
    bindViewTap () {
      const url = '../logs/main'
      if (mpvuePlatform === 'wx') {
        mpvue.switchTab({ url })
      } else {
        mpvue.navigateTo({ url })
      }
    },
    clickHandle (ev) {
      console.log('clickHandle:', ev)
      // throw {message: 'custom test'}
    }
  },

  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>

</style>
