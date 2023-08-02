<template>
  <div class="iframe-component">
    <iframe class="iframe-style" id="casinoIframe"
      title="Casino Iframe"
      width="100%"
      height="1000px"
      src="https://jazz-casino-lobby.azurewebsites.net/?token=VEVTVDE6cHBoMWE%3D&playerId=Mzk1NA%3D%3D&language=es&casinoClient=MR_REELS">
    </iframe>
  </div>
</template>

<script>
  export default {
    name: "CasinoPage",

    setup:() => {
      const BackEndUrl = "empelotados.mx";
      
      return {
        BackEndUrl,
      }
    },
  }
</script>