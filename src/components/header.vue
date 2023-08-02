<template>
  <header class="header">
    <div class="header-content">
      <div class="header-content__nav">
        <menu-component />
        <div class="header-content__nav--img">
          <a href="/">
            <img class="header-content__img" src="../assets/images/logo.png" alt="mrs reels logo" />
          </a>
        </div>
        <div class="header-content__cta">
          <button class="header-content__cta--join primary-button primary-button__classic" @click="openModal">Únete a Nosotros</button>
          <div class="header-buttons">
            <button class=" primary-button primary-button__register" @click="openRegisterModal">Registro</button>
            <a href="#" class=" primary-button primary-button__register" @click="openModal">Ingresar</a>
          </div>
        </div>
      </div>
      <div class="header-content__second">
        <ul class="header-content__info--list">
          <li class="header-content__info--list-item">
            <router-link to="/sportsbook">Deportes</router-link>
          </li>
          <li class="header-content__info--list-item">
            <router-link to="/live-betting">En vivo</router-link>
          </li>
          <li class="header-content__info--list-item">
            <router-link to="/casino">Casino</router-link>
          </li>
          <li class="header-content__info--list-item">
            <router-link to="promotions">Casino en vivo</router-link>
          </li>
          <li class="header-content__info--list-item">
            <router-link to="/racebook">Caballos</router-link>
          </li>
          <li class="header-content__info--list-item">
            <router-link to="/props-builder">Crea tus props</router-link>
          </li>
        </ul>
        <div class="header-content__second--time">
          <a href="#">Promociones</a>
          <clock />
        </div>
      </div>
    </div>
    <ModalComponent ref="modal" />
    <ModalRegister ref="modalRegister"/>
  </header>
</template>

<script>
import ModalRegister from '@/components/modal-register.vue';
import ModalComponent from '@/components/modal.vue';
import Clock from '@/components/Clock.vue';
// import SelectLenguage from './select-lenguage.vue';
import MenuComponent from '@/components/menu.vue'

export default {
  name: "HeaderComponent",
  components: {
    ModalComponent,
    Clock,
    ModalRegister,
    // SelectLenguage,
    MenuComponent
  },
  methods: {
    openModal() {
      this.$refs.modal.openModal();
    },
    openRegisterModal() {
      this.$refs.modalRegister.openRegisterModal();
    }
  },
  setup() { },
};
</script>
