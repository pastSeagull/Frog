<template>
<div class="swiper">
  <swiper :options="swiperOption">
    <!-- slides -->
    <!-- <swiper-slide v-for="list of SwiperList" :key="list.id"><img class="swiper-img" :src="list.img" alt=""></swiper-slide> -->
    <swiper-slide><img class="swiper-img" src="../../../assets/images/lb1.jpg" alt=""></swiper-slide>
    <swiper-slide><img class="swiper-img" src="../../../assets/images/lb1.jpg" alt=""></swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data() {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      SwiperList: [{
        id: '1',
        img: '../../../assets/images/lb1.jpg'
      },
      {
        id: '2',
        img: '../../../assets/images/lb1.jpg'
      }]
    }
  }
}
</script>

<style scoped>
.swiper >>> .swiper-pagination-bullet-active{
  background: red !important;
}
.swiper{
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 40%;
  background: #eee;
}
.swiper-img{
  width: 100%;
}
</style>
