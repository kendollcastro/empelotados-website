<template>
  <div class="swiper-container">
    <div class="swiper-wrapper">
      <div class="swiper-slide" v-for="(item, index) in items" :key="index">
        <!-- Muestra la imagen en cada slide -->
        <picture>
          <source media="(max-width: 744px)" :srcset="item.imageSrcMobile" />
          <img :src="item.imageSrcDesktop" :alt="item.imageAlt" class="slide-image" />
        </picture>
        
      </div>
    </div>
    <div class="swiper-pagination"></div>
  </div>
</template>

<script>
import SwiperCore, { Autoplay, Mousewheel, Pagination } from 'swiper/core';
import 'swiper/swiper-bundle.css';

SwiperCore.use([Autoplay, Mousewheel, Pagination]);

export default {
  props: {
    items: {
      type: Array,
      required: true,
    },
  },
  mounted() {
    this.initSwiper();
  },
  methods: {
    initSwiper() {
      this.swiper = new SwiperCore('.swiper-container', {
        direction: 'vertical',
        slidesPerView: 1,
        spaceBetween: 30,
        mousewheel: false,
        autoplay: {
          delay: 3000,
          disableOnInteraction: false,
        },
      });
    },
  },
  beforeUnmount() {
    if (this.swiper) {
      this.swiper.destroy();
    }
  },
};
</script>

