<template>
  <div class="modal-backdrop" v-if="showModal">
    <div class="modal-content__heading">
      <div class="modal-content__heading--text">
        <h3>Ingresar</h3>
        <button class="close-button" @click="closeModal">
          <span class="material-symbols-rounded">cancel</span>
        </button>
      </div>
      <div class="modal-content__heading--img">
        <img src="../../src/assets/images/logo.png" alt="">
      </div>
    </div>
    <div class="modal-content">
      <!-- Contenido de tu modal aquí -->
      <form class="login__form" name="LoginForm" action="javascript:void(0)" onsubmit="BackEndLogin(this); return false">
        <div class="login__form--item">
          <label class="login__form--label" for="username">Usuario</label>
          <input class="login__form--input" name="username" id="username" type="text" required/>
        </div>

        <div class="login__form--item">
          <label class="login__form--label" for="password">Contraseña</label>
          <input class="login__form--input" :type="passwordVisible ? 'text' : 'password'" v-model="password" name="password" id="password" required/>
          <span class="password-toggle material-symbols-rounded" @click="togglePasswordVisibility">
            {{ passwordVisible ? 'visibility_off' : 'visibility' }}
          </span>
        </div>
        
        <div class="text-center mt-2"> 
          <span name="msj_loading" id="id-login-loading"></span>
          <small class="text-danger" name="msj_error_lg"></small>
        </div>

        <div class="login__link">
          <div class="login__link--remember">
            <!-- <label for="remember">Remember me</label> -->
            <!-- <input type="checkbox"> -->
          </div>

          <a :href="`https://apuestas.${BackEndUrl}/home/reset-pass`">olvidaste tu contraseña?</a>
        </div>
        
        <div class="login__btns-login">
          <input type="submit" class="btn-login secondary-button secondary-button__login" name="send" id="send" value="Ingresar">
          <input type="hidden" name="BackEndUrl" :value="`https://apuestas.${BackEndUrl}`">

          <router-link to="/registrarme" class="secondary-button secondary-button__register-secondary" @click="closeModal">Registrarme</router-link>
        </div>        
      </form>
    </div>
  </div>
</template>

<script>
  import { ref } from 'vue';
  export default {
    name: 'ModalComponent',
    setup:() => {
      const BackEndUrl = "empelotados.mx";


      const password = ref('');
      const passwordVisible = ref(false);

      const togglePasswordVisibility = () => {
        passwordVisible.value = !passwordVisible.value;
      };
      
      return {
        BackEndUrl,
        password,
        passwordVisible,
        togglePasswordVisibility,
      }
    },
    data() {
      return {
        showModal: false
      }
    },
    methods: {
      openModal() {
        this.showModal = true;
      },
      closeModal() {
        this.showModal = false;
      }
    }
  }
</script>