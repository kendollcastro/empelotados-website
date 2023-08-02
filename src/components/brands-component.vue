<template>
  <section class="brands animate-fade-down animate-once" >
    <div class="brands-content">
      <button class="brands-content__button" v-for="(brand, index) in brands" :key="index">
        <img :src="brand.svg" :alt="brand.alt">
      </button>
    </div>
  </section>
</template>

<script>
export default {
  name: "ImageComponent",
  setup() {
    return {
      brands: [
        {
          svg   : require('@/assets/images/brands/visa.svg'),
          alt   : 'Visa',
        },
        {
          svg   : require('@/assets/images/brands/master.svg'),
          alt   : 'Visa',
        },
        {
          svg   : require('@/assets/images/brands/oxxo.svg'),
          alt   : 'Visa',
        },
        {
          svg   : require('@/assets/images/brands/seven.svg'),
          alt   : 'Visa',
        },
        {
          svg   : require('@/assets/images/brands/walmart.svg'),
          alt   : 'Visa',
        },
        {
          svg   : require('@/assets/images/brands/soriana.svg'),
          alt   : 'Visa',
        },
        {
          svg   : require('@/assets/images/brands/circle.svg'),
          alt   : 'Visa',
        }
      ],
    }
  }
};
</script>
