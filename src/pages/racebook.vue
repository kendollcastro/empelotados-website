<template>
  <iframe title="racebook" width="100%" height="1500px" id="iframe-signup-page" class="cs-iframe-signup-page iframe-general-top" src="https://racebookboss.wintek.live/BOSSWagering/Racebook/InternetBetTaker2021-06/Racebook.aspx"></iframe>
</template>

<script>
  export default {
    name: "RacebookPage",

    setup:() => {
      const BackEndUrl = "empelotados.mx";
      
      return {
        BackEndUrl,
      }
    },
  }
</script>