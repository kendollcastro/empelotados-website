<template>
  <iframe title="sportbook" class="m-auto p-auto d-flex iframe-general-top" :src="`https://apuestas.${BackEndUrl}/mainbk/classicmain`" name="iframe_cards" width="100%" height="900px"></iframe>
</template>

<script>
  export default {
    name: "SportsBookPage",

    setup:() => {
      const BackEndUrl = "empelotados.mx";
      
      return {
        BackEndUrl,
      }
    },
  }
</script>