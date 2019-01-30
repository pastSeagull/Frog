<template>
<div class="head-box">
  <div class="head-left">
    <div class="iconfont back-icon">&#xe624;</div>
  </div>
  <div class="head-search"><span class="iconfont">&#xe632;</span>搜索城市或景点</div>
  <div class="head-right">城市<span class="iconfont arrow-icon">&#xe600;</span></div>
</div>
</template>

<script>
export default {
  name: 'HomeHead'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles'
.head-box{
  display: flex;
  line-height: .86rem;
  background: $bgColor;
  color: #fff;
}
.head-box .head-left{
  width: .64rem;
  float: left;
}
.head-box .head-left .back-icon{
  text-align: center;
  font-size: .4rem;
}
.head-box .head-search{
  padding-left: .3rem;
  height: .64rem;
  line-height: .64rem;
  flex: 1;
  background: #fff;
  border-radius: .1rem;
  margin-top: .12rem;
  margin-left: .2rem;
  color: #686868;
}
.head-box .head-right{
  width: 1.24rem;
  float: right;
  text-align: center;
}
.head-box .head-right span{
  margin-left: .1rem;
  font-size: .24rem;
}
</style>
