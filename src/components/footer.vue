<template>
  <footer class="footer">
    <div class="footer-content">
      <ul class="footer-content__list">
        <h3 class="footer-content__list--title">Reglas</h3>
        <li class="footer-content__list--item" @click="isActive = !isActive" v-for="(route, index) in rules" :key="index">
          <router-link :to="route.route">{{ route.name }}</router-link>
        </li>
      </ul>
      <ul class="footer-content__list">
        <h3 class="footer-content__list--title">Nuestras políticas</h3>
        <li class="footer-content__list--item" @click="isActive = !isActive" v-for="(route, index) in legal" :key="index">
          <router-link :to="route.route">{{ route.name }}</router-link>
        </li>
      </ul>
      <ul class="footer-content__list">
        <h3 class="footer-content__list--title">Legal</h3>
        <li class="footer-content__list--item" @click="isActive = !isActive" v-for="(route, index) in regulations"
          :key="index">
          <router-link :to="route.route">{{ route.name }}</router-link>
        </li>
      </ul>
    </div>
    <div class="footer-social">
      <ul class="footer-social__items">
        <li class="footer-social__items--item" v-for="(social, index) in social" :key="index">
          <a :href="social.link" target="_blank">
            <img :src="social.img" :alt="social.alt">
          </a>
        </li>
      </ul>
    </div>
    <div class="footer-warranty">
      <ul class="footer-warranty__items">
        <li class="footer-warranty__items--item" v-for="(warranty, index) in warranty" :key="index">
          <img :src="warranty.img" :alt="warranty.alt">
        </li>
      </ul>
    </div>
    <div class="footer-text">
      <ul class="footer-text__items">
        <li class="footer-text__items--item" v-for="(text, index) in text" :key="index">
          <p>{{ text.text }}</p>
        </li>
      </ul>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent",
  setup() {
    return {
      rules: [
        {
          name    : 'Reglas de la casa',
          route   : 'reglas-casa'
        },
        {
          name    :  'Reglas de deportes',
          route   :  'sports-rules'
        },
        {
          name    : 'Reglas de casino',
          route   : 'reglas-casino'
        },
        {
          name    : 'Preguntas Frecuentes',
          route   : 'preguntas-frecuentes'
        },
      ],
      legal: [
        {
          name  : 'Pagos y Retiros Anticipados',
          route : 'pagos-retiros'
        },
        {
          name  : 'Política de Cookies',
          route : 'politica-cookies'
        },
        {
          name  : 'Política de Retiradas',
          route : 'politica-retiradas'
        },
        {
          name  : 'Mapa del Sitio',
          route : 'auto-exclusion'
        }
      ],
      regulations: [
        {
          name: 'Terminos y condiciones',
          route: 'terminos-condiciones'
        },
        {
          name: 'Políticas de privacidad',
          route: 'politica-privacidad'
        },
        {
          name: 'Políticas de juego responsable',
          route: 'juego-responsable'
        },
        {
          name: 'Juego justo',
          route: 'juego-justo'
        },
      ],
      social: [
        {
          name    : 'facebook',
          link    : 'https://www.facebook.com/empelotadosofic',
          img     : require('@/assets/images/footer/facebook.svg'),
          alt     : 'facebook'
        },
        {
          name    : 'tiktok',
          link    : 'https://www.tiktok.com/@empelotados.mx',
          img     : require('@/assets/images/footer/tiktok.png'),
          alt     : 'tiktok'
        },
        {
          name    : 'instagram',
          link    : 'https://www.instagram.com/empelotados.mx/',
          img     : require('@/assets/images/footer/insta.svg'),
          alt     : 'instagram'
        },
        {
          name    : 'youtube',
          link    : 'https://www.youtube.com/@empelotadosoficial',
          img     : require('@/assets/images/footer/youtube.png'),
          alt     : 'youtube'
        },
        {
          name    : '+18',
          link    : '',
          img     : require('@/assets/images/footer/18.svg'),
          alt     : '+18'
        },
      ],
      warranty: [
        {
          name    : 'ssl',
          img     : require('@/assets/images/footer/ssl.svg'),
          alt     : 'ssl'
        },
        {
          name    : 'segob',
          img     : require('@/assets/images/footer/segob.svg'),
          alt     : 'segob'
        },
        {
          name    : 'juego responsable',
          img     : require('@/assets/images/footer/juego.svg'),
          alt     : 'juego responsable'
        },
      ],
      text: [
        {
          text    : 'Empelotados.mx es operada por OPERADORA DE ENTRETENIMIENTO JUPITER S.A DE C.V., una compañía registrada en México, autorizada y regulada por la Secretaría de Gobernación- Dirección de Juegos y Sorteos- República Mexicana. (SEGOB DGJS/1832/2023), en conjunto con el permisionario Juegos y Sorteos de Jalisco S.A de C.V. Empelotados mantiene una licencia de apuestas interactivas para la prestación de apuestas en actividades deportivas.'
        },
        {
          text    : '2023 Empelotados.mx. Todos los Derechos Reservados. Empelotados.mx es un sitio de OPERADORA DE ENTRETENIMIENTO JUPITER S.A DE C.V., LOS JUEGOS CON APUESTA ESTAN PROHIBIDOS PARA MENORES DE EDAD'
        },
        {
          text    : 'Empelotados es una marca registrada, propiedad de Servicios INCA S de R.L. de C.V.'
        },
      ]
    }
  },
};
</script>
