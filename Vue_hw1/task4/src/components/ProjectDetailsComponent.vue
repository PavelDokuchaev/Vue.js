<template>
  <div class="banner"></div>

  <div class="description">
    <h1 class="description__title">{{ header }}</h1>
    <p class="description__text">{{ text1 }}</p>
    <p class="description__text">{{ text2 }}</p>
  </div>

  <swiper :style="{
    '--swiper-navigation-color': '#fff',
    '--swiper-pagination-color': '#fff',
  }" :zoom="true" :navigation="true" :pagination="{
  clickable: true,
}" :modules="modules" class="mySwiper">
    <swiper-slide>
      <div class="swiper-zoom-container">
        <img :src='bedroom1' alt="">
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="swiper-zoom-container">
        <img :src='bedroom2' alt="">
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="swiper-zoom-container">
        <img :src='bedroom3' alt="">
      </div>
    </swiper-slide>
  </swiper>
</template>

<script>
import { mapState } from 'vuex';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';

import 'swiper/css/zoom';
import 'swiper/css/navigation';
import 'swiper/css/pagination';

import { Zoom, Navigation, Pagination } from 'swiper/modules';
import bedroom1 from '../assets/img/bedroompj.png';
import bedroom2 from '../assets/img/bedroom.jpg';
import bedroom3 from '../assets/img/bedroom2.jpg';

export default {
  components: { Swiper, SwiperSlide },
  setup() {
    return {
      modules: [Zoom, Navigation, Pagination],
    };
  },
  data() {
    return {
      bedroom1: bedroom1,
      bedroom2: bedroom2,
      bedroom3: bedroom3,
    }
  },
  computed: {
    ...mapState(['header', 'text1', 'text2'])
  }
}

</script>

<style lang="scss" scoped>
body {
  position: relative;
  height: 100%;
}

.banner {
  background-image: url('../assets/img/bannerpj.png');
  background-repeat: no-repeat;
  height: 356px;
  background-size: cover;
  margin-bottom: 150px;
}

.description {
  padding-left: calc(50% - 329px);
  padding-right: calc(50% - 329px);
  display: flex;
  flex-direction: column;
  margin-bottom: 100px;
  gap: 12px;

  &__title {
    color: #292F36;
    font-family: DM Serif Display;
    font-size: 50px;
    font-style: normal;
    font-weight: 400;
    line-height: 125%;
    letter-spacing: 1px;
  }

  &__text {
    color: #4D5053;
    font-family: Jost;
    font-size: 22px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    letter-spacing: 0.22px;
  }
}

.swiper {
  width: 100%;
  height: 100%;
  margin-bottom: 50px;
}

.swiper-slide {
  overflow: hidden;
}

img {
  border-radius: 55px;
  width: 1200px;
}
</style>
<style>
.swiper-pagination {
  position: unset;
  margin-bottom: 100px;
}

.swiper-pagination-bullet {
  border: 1px solid #000;
  background: none;
  opacity: 1;
  width: 15px;
  height: 15px;
}

.swiper-pagination-bullet:hover {
  background: #4D5053;
}

.swiper-wrapper {
  margin-bottom: 20px;
}
</style>