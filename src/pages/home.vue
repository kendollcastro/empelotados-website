<template>
  <!-- <hero-slider /> -->
  <slider-hero :items="slides"/>
  <options-anchors/>
  <games-cards/>
  <!-- <games-tabs/> -->
  <!-- <slider-nuevo/> -->
  <image-component />
  <!-- <banner-component :image="image" altImage="Slider image" /> -->
  <!-- <banner-info /> -->
</template>

<script>
// import HeroSlider from "@/components/hero-slider.vue";
// import GamesTabs from "@/components/games-tabs.vue";
// import SliderNuevo from '@/components/slider-nuevo.vue'
// import BannerComponent from "@/components/banner-component.vue";
// import BannerInfo from "@/components/banner-info.vue";
import ImageComponent from "@/components/brands-component.vue";
import SliderHero from '@/components/slider-hero.vue';
import OptionsAnchors from '@/components/options-anchors.vue';
import GamesCards from '@/components/games-cards.vue';

export default {
  name: "PageHome",
  components: {
    // HeroSlider,
    // SliderNuevo,
    // GamesTabs,
    // BannerComponent,
    ImageComponent,
    // BannerInfo,
    SliderHero,
    OptionsAnchors,
    GamesCards,
  },

  setup: () => {
    /* Hero Banner Variables */
    const image = require("@/assets/images/logo.png");
    return {
      image,
    };
  },

  data() {
    return {
      slides: [
        { 
          imageSrcDesktop: require('@/assets/images/slider/slider-hero.jpg'), 
          imageAlt: 'Imagen 1',
          imageSrcMobile: require('@/assets/images/slider/slider-hero-mobile.jpg'),
        },
        { 
          imageSrcDesktop: require('@/assets/images/slider/slider-hero.jpg'), 
          imageAlt: 'Imagen 1',
          imageSrcMobile: require('@/assets/images/slider/slider-hero-mobile.jpg'),
        },
        { 
          imageSrcDesktop: require('@/assets/images/slider/slider-hero.jpg'), 
          imageAlt: 'Imagen 1',
          imageSrcMobile: require('@/assets/images/slider/slider-hero-mobile.jpg'),
        }
        // Agrega más objetos según la cantidad de slides que desees mostrar
      ],
    };
  },
};
</script>