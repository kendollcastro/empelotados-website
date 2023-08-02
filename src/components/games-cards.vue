<template>
  <section class="games-cards">
    <div class="games-cards__container">
      <div v-for="(card, index) in cards" :key="index" class="games-cards__container--card">
        <img :src="card.img" alt="">
        <h3>{{ card.title }}</h3>
        <a :href="card.link" class="games-cards__container--card-btn">Jugar ahora</a>
      </div>
    </div>
  </section>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'GamesCards',
  setup() {
    const cards = [
      {
        title      : 'Deportes',
        link       : 'https://www.example.com',
        img        : require('@/assets/images/games-cards/games-card-sports.png'),
        alt        : ''
      },
      {
        title      : 'Casino',
        link       : 'https://www.example.com',
        img        : require('@/assets/images/games-cards/games-card-casino.png'),
        alt        : ''
      },
      {
        title      : 'Casino en vivo',
        link       : 'https://www.example.com',
        img        : require('@/assets/images/games-cards/games-card-casino-live.png'),
        alt        : ''
      },
      {
        title      : 'Juegos Virtuales',
        link       : 'https://www.example.com',
        img        : require('@/assets/images/games-cards/games-card-virtual.png'),
        alt        : ''
      }
      // Agrega más objetos según la cantidad de cards que desees mostrar
    ];

    const showButton = ref(Array(cards.length).fill(false)); // Arreglo reactiva para controlar la visibilidad del botón

    return {
      cards,
      showButton,
    };
  },
};
</script>
