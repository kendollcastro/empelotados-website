<template>
  <Carousel :autoplay="2000"  :transition="2300" :wrapAround="true" :touchDrag="false" :mouseDrag="true">
    <Slide v-for="(slide, index) in slides" :key="index" aria-hidden="true">
      <div class="carousel__item hero-slider">
        <div class="hero-slider__info">
          <div class="hero-slider__info--container">
            <div class="hero-slider__text">
              <h1 class="hero-slider__text-title">{{ slide.title }}</h1>
              <div class="hero-slider__text-btn--desktop" v-show="slide.btn">
                <button @click="openModal" class="primary-button primary-button__register hero-slider__apost" aria-hidden="true">{{ slide.btn }}</button>
              </div>
            </div>
            <div class="hero-slider__slider-img" v-if="slide.sliderImg != null ">
              <img class="hero-slider__slider-img--content" :src="slide.sliderImg" alt="" loading="lazy">
            </div>
            <div class="hero-slider__text-btn" v-show="slide.btn">
              <button @click="openModal" class="primary-button primary-button__register hero-slider__apost" aria-hidden="true">{{ slide.btn }}</button>
            </div>
          </div>
        </div>
        <div class="hero-slider__bg">
          <img :src="slide.bgImage" :alt="slide.alt" v-preload="slide.bgImage">
        </div>
      </div>
    </Slide>

    <template #addons>
      <div class="hero-slider__pagination">
      </div>
    </template>
  </Carousel>
  <ModalComponent ref="modal" />
</template>

<script>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide } from 'vue3-carousel'
import ModalComponent from '@/components/modal.vue'

export default {
  name: 'Hero-Basic',
  components: {
    Carousel,
    Slide,
    // Pagination,
    ModalComponent
  },
    methods: {
      openModal() {
        this.$refs.modal.openModal();
      }
  },
  data() {
    
    return {
      slides: [
      {
        title      :  'Slots',
        subtitle   :  'Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, iste.',
        alt        :  'Lorem ipsum',
        bgImage    :  require('../assets/images/slider_slots.jpg'),
        sliderImg  :  require('../assets/images/element-01.png'),
        route      :  "sportsbook",
        btn        :  "Registrarse"
      },
      {
        title      :  'Casino en vivo',
        subtitle   :  'Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, iste.',
        alt        :  'Lorem ipsum',
        bgImage    :  require('../assets/images/slider_casino.jpg'),
        sliderImg  :  require('../assets/images/element-02.png'),
        route      :  "casino",
        btn        :  "Depositar"
      },
      {
        title      :  'Promotions',
        subtitle   :  'Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, iste.',      
        alt        :  'Lorem ipsum',
        bgImage    :  require('../assets/images/slider_promotions.jpg'),
        sliderImg  :  require('../assets/images/element-03.png'),
        route      :  "racebook",
        btn        :  "Depositar"
      }
      ]
    }
  }
}
</script>
