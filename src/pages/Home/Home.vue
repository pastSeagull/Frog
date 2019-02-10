<template>
  <div>
    <home-head></home-head>
    <home-swiper></home-swiper>
    <home-icon></home-icon>
  </div>
</template>

<script>
import HomeHead from './compoheht/Header'
import HomeSwiper from './compoheht/Swiper'
import HomeIcon from './compoheht/Icon'
export default {
  name: 'Home',
  components: {
    HomeHead,
    HomeSwiper,
    HomeIcon
  }
}
</script>

<style lang="stylus" scoped>

</style>
