<template>
  <iframe title="prop builder" class="liveBettingIframe iframe-general-top" :src="`https://bv2.digitalsportstech.com/betbuilder?sb=jazz&theme=jazz&language=es-es`" width="100%" height="900px"></iframe>
</template>

<script>
  export default {
    name: "PropsBuilderPage",

    setup:() => {
      const BackEndUrl = "betcasino";
      
      return {
        BackEndUrl,
      }
    },
  }
</script>