<template>
  <div>
    <home-head></home-head>
    <home-swiper></home-swiper>
  </div>
</template>

<script>
import HomeHead from './compoheht/Header'
import HomeSwiper from './compoheht/Swiper'
export default {
  name: 'Home',
  components: {
    HomeHead,
    HomeSwiper
  }
}
</script>

<style lang="stylus" scoped>

</style>
