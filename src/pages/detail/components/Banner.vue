<template>
  <div>
    <div class="banner" @click="handleBannerClick" >
      <img
        class="banner-img"
        src="http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_600x330_bf9c4904.jpg"/>
      <div class="banner-info">
        <div class="banner-title">大连圣亚海洋世界(AAAA景区)</div>
        <div class="banner-num"><span class="iconfont banner-icon">&#xe625;</span>39</div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @gallaryclose="handleGallaryClick"></common-gallary>
  </div>
</template>

<script>
  import CommonGallary from 'common/gallary/Gallary'

  export default {
    name: "Banner",
    data(){
      return{
        showGallary:false,
        imgs:['http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_800x800_70debc93.jpg',
          'http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_800x800_70debc93.jpg']
      }
    },
    components: {
      CommonGallary
    },
    methods:{
      handleBannerClick(){
        this.showGallary =true
      },
      handleGallaryClick(){
        this.showGallary =false
      }
    }
  }
</script>

<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      display flex
      position absolute
      left 0
      right 0
      bottom 0
      color #fff
      line-height .6rem
      .banner-title
        flex 1
        padding 0 .2rem
        font-size .32rem
      .banner-num
        padding 0 .4rem
        height .32rem
        margin-top .14rem
        line-height .4rem
        border-radius .2rem
        background rgba(0, 0, 0, 0.8)
      .banner-icon
        font-size .24rem
</style>
