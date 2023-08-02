<template>
  <div class="iframe-component">
    <iframe class="iframe-style" id="casinoGamesIframe"
      title="Juegos Casino"
      width="100%"
      height="1000px"
      src="https://jazz-casino-lobby.azurewebsites.net/?token=dGVzdGxvYmJ5OnRlc3Q%3D&playerId=Mzk1NA%3D%3D&language=es&casinoClient=MR_REELS_LIVE">
    </iframe>
  </div>
</template>

<script>
  export default {
    name: "JuegosCasinoPage",

    setup:() => {
      const BackEndUrl = "mrsreels.com";
      
      return {
        BackEndUrl,
      }
    },
  }
</script>