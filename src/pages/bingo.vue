<template>
  <div class="iframe-component">
    <iframe class="iframe-style" id="bingoIframe"
      title="Bingo Iframe"
      width="100%"
      height="1000px"
      src="https://jazz-casino-lobby.azurewebsites.net/?token=dGVzdGxvYmJ5OnRlc3Q%3D&playerId=Mzk1NA%3D%3D&language=es&casinoClient=MR_REELS_BINGO">
    </iframe>
  </div>
</template>

<script>
  export default {
    name: "BingoPage",

    setup:() => {
      const BackEndUrl = "mrsreels.com";
      
      return {
        BackEndUrl,
      }
    },
  }
</script>