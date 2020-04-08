<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt width="640" height="214" />
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/p/tts0/1609/96/32fe674b30c87202.jpg_r_480x320x95_a8494fdf.jpg',
        title: '圆明园',
        desc: '百年皇家的珍宝，民族耻辱的见证'
      },
      {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/p/tts0/1609/96/32fe674b30c87202.jpg_r_480x320x95_a8494fdf.jpg',
        title: '圆明园',
        desc: '百年皇家的珍宝，民族耻辱的见证'
      },
      {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/p/tts0/1609/96/32fe674b30c87202.jpg_r_480x320x95_a8494fdf.jpg',
        title: '圆明园',
        desc: '百年皇家的珍宝，民族耻辱的见证'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl';

.recommend-title {
  margin-top: 0.2rem;
  line-height: 0.8rem;
  background-color: #eee;
  text-indent: 0.2rem;
}

.item-img-wrapper {
  overflow: hidden;
  height: 0;
  padding-bottom: 33.9%;

  .item-img {
    width: 100%;
  }
}

.item-info {
  padding: 0.1rem;

  .item-title {
    line-height: 0.54rem;
    font-size: 0.32rem;
    ellipsis();
  }

  .item-desc {
    line-height: 0.4rem;
    color: #ccc;
    ellipsis();
  }
}
</style>
