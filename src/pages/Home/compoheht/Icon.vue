<template>
<div>
  <div class="icon-box">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="list of page" :key="list.id">
          <a href="">
              <div class="img-box">
                <img class="icon-img" :src="list.imgurl" alt="">
              </div>
            <span>{{list.txt}}</span>
            </a>
        </div>
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
  <ul class="icon-ul">
    <li class="icon-li"><span class="iconfont">&#xe611;</span>定位失败</li>
      <li class="icon-li"><span class="iconfont">&#xe76c;</span><a href="">必游榜单</a></li>
  </ul>
</div>
</template>

<script>
export default {
  name: 'HomeIcon',
  data() {
    return {
      swiperOption: {
        pagination: '.swiper-pagination'
      },
      icon: [{
        id: '1',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        txt: '景点门票'
      }, {
        id: '2',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
        txt: '一日游'
      }, {
        id: '3',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
        txt: '南宁必备'
      }, {
        id: '4',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
        txt: '游乐场'
      }, {
        id: '5',
        imgurl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20191/de711920c71e38287d9f95f7910aa1aa.png',
        txt: '精品小团'
      }, {
        id: '6',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1803/f5/a963333e1fa802.png',
        txt: '本地游玩'
      }, {
        id: '7',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
        txt: '动植物园'
      }, {
        id: '8',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
        txt: '海洋馆'
      }, {
        id: '9',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png',
        txt: '泡温泉'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.icon.forEach((list, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(list)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.icon-box{
  margin-top: .20rem;
  overflow: hidden;
  height: 0;
  padding-bottom: 50%;
}
.icon-box >>> .swiper-container{
  height: 0;
  padding-bottom: 50%;
}
.icon-box .icon{
  position: relative;
  float: left;
  width: 25%;
  padding-bottom: 20%;
}
.icon-box .icon a span{
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  text-align: center;
  color: #000;
  font-size: .30rem;
  ellipsis()
}
.icon-box .icon .img-box{
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: .30rem;
}
.icon-box .icon .img-box .icon-img{
  display: block;
  margin: 0 auto;
  height: 80%;
}
.icon-ul{
  border-top: .01rem solid #ccc;
}
.icon-ul .icon-li{
  float: left;
  width: 49%;
  height: 1rem;
  line-height: 1rem;
  text-align: center;
  border-left: .01rem solid #ccc;
}
</style>
