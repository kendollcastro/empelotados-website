<template>
  <div class="modal-backdrop" v-if="showRegisterModal">
    <div class="modal-register">
      <div class="modal-register__heading">
        <div class="modal-register__heading--text">
          <h3>Registrarse</h3>
          <button class="close-button" @click="closeRegisterModal">
            <span class="material-symbols-rounded">cancel</span>
          </button>
        </div>
      </div>
      <div class="modal-register__content">
        <div class="modal-content__img">
          <img src="../../src/assets/images/modal-register-img.png" alt="">
          <div class="modal-register__heading--img">
            <img src="../../src/assets/images/logo.png" alt="empelotados">
            <p>Por favor complete todos los campos de este formulario</p>
          </div>
        </div>
        <div class="modal-content__iframe">
          <iframe class="iframe-style" id="registerIframe"
          title="Registro Iframe"
          width="100%"
          height="684px"
          :src="`https://apuestas.${BackEndUrl}/sign-up`">
        </iframe> 
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'ModalRegister',
    setup:() => {
      const BackEndUrl = "empelotados.mx";
      
      return {
        BackEndUrl,
      }
    },
    data() {
      return {
        showRegisterModal: false
      }
    },
    methods: {
      openRegisterModal() {
        this.showRegisterModal = true;
      },
      closeRegisterModal() {
        this.showRegisterModal = false;
      }
    }
  }
</script>