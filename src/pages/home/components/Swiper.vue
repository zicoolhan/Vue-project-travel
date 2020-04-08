<template>
  <div class="wrapper">
    <swiper :options="swiperOption" ref="mySwiper">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" v-bind:key="item.id">
        <img
          class="swiper-img"
          :src= "item.imgUrl"
          width="375"
          height="117"
        />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        autoplay: 5000,
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://img1.qunarzz.com/sight/p0/1705/63/63a8c5c44180cc91a3.img.jpg_600x330_69ce7947.jpg'
      },
      {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/57/579b6c97900745db.water.jpg_600x330_a7a104d2.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
// 穿透？
.wrapper >>> .swiper-pagination-bullet-active {
  background: #fff !important;
}

.wrapper {
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 31.25%;

  .swiper-img {
    width: 100%;
  }
}
</style>
