<template>
<div class="swiper">
  <swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide v-for="list of SwiperList" :key="list.id"><img class="swiper-img" :src='list.img' alt=""></swiper-slide>
    <!-- <swiper-slide><img class="swiper-img" src="../../../assets/images/lb1.jpg" alt=""></swiper-slide>
    <swiper-slide><img class="swiper-img" src="../../../assets/images/lb1.jpg" alt=""></swiper-slide> -->
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
        img: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20191/60196dcb4b77616ab27e5ee9ad9d9f76.jpg_750x200_0c7e0a36.jpg'
      }, {
        id: '2',
        img: 'http://img1.qunarzz.com/piao/fusion/1812/d6/daa880b254940402.jpg_750x200_b114308a.jpg'
      }]
    }
  },
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
  padding-bottom: 27%;
  background: #eee;
}
.swiper-img{
  width: 100%;
}
</style>
