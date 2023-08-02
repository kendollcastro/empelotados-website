<template>
  <div class="iframe-component">
    <iframe class="iframe-style" id="registerIframe"
      title="Registro Iframe"
      width="100%"
      height="1000px"
      :src="`https://apuestas.${BackEndUrl}/sign-up`">
    </iframe>
  </div>
</template>

<script>
  export default {
    name: "RegistrarmePage",

    setup:() => {
      const BackEndUrl = "empelotados.mx";
      
      return {
        BackEndUrl,
      }
    },
  }
</script>