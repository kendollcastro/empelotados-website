<template>
  <div class="hamburger-menu">
    <button class="hamburger-menu__button" @click="isActive = !isActive" :class="{ 'is-active': isActive }">
      <span class="material-symbols-rounded header-content__icon">menu</span>
    </button>
    <ul class="hamburger-menu__list" :class="{ 'is-active': isActive }">
      <div class="hamburger-menu__list--header">
        <p>Menu</p>
        <button @click="isActive = !isActive" class="hamburger-menu__close-button" aria-label="Cerrar menú"><span class="material-symbols-rounded header-content__icon">menu</span></button>
      </div>
      <li class="hamburger-menu__item" @click="isActive = !isActive" v-for="(route, index) in routes" :key="index">
        <router-link :to="route.route">{{ route.name }}</router-link>
        <span class="material-symbols-rounded">chevron_right</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "MenuComponent",
  data() {
    return {
      isActive: false,
      routes: [
        {
          name       :  'Deportes',
          route      :  'sportsbook'
        },
        {
          name       :  'En vivo',
          route      :  'racebook'
        },
        {
          name       :  'Casino',
          route      :  'live-betting'
        },
        {
          name       :  'Casino en vivo',
          route      :  'casino'
        },
        {
          name       :  'Caballos',
          route      :  'props-builder'
        },
      ]
    };

  },
};
</script>
