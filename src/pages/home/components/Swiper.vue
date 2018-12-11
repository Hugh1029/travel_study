<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id" >
        <img class="swiper-img" :src="item.url"/>
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        url: 'http://img1.qunarzz.com/piao/fusion/1812/e5/f7e2e687a0a04d02.jpg_890x330_73c29eba.jpg'
      }, {
        id: '0002',
        url: 'http://img1.qunarzz.com/piao/fusion/1806/6a/fbc217b49175cc02.jpg_890x330_8017a980.jpg'
      }, {
        id: '0003',
        url: 'http://img1.qunarzz.com/piao/fusion/1812/61/173390b5080a202.jpg_890x330_f3412cb2.jpg'
      }, {
        id: '0004',
        url: 'http://img1.qunarzz.com/piao/fusion/1811/21/cc5f839caac02702.jpg_890x330_29064459.jpg'
      }, {
        id: '0005',
        url: 'http://img1.qunarzz.com/piao/fusion/1811/d8/2977624617721802.jpg_890x330_39ab9791.jpg'
      }, {
        id: '0006',
        url: 'http://img1.qunarzz.com/piao/fusion/1809/b6/23980fda69a67d02.jpg_890x330_fe885a29.jpg'
      }, {
        id: '0007',
        url: 'http://img1.qunarzz.com/piao/fusion/1811/c2/cf99d28bb0ac8b02.jpg_890x330_81ad66fd.jpg'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #ffffff!important
  .wrapper
    width: 100%
    height: 0
    padding-bottom: 31.25%
    background-color: #eee
    .swiper-img
      width: 100%
</style>
