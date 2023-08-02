<template>
  <div class="clock">
    <span class="material-symbols-rounded">schedule</span>
    <p>{{ currentTime }} (GMT-6)</p>
  </div>
</template>

<script>
import moment from "moment-timezone";

export default {
  name: "ClockComponent",
  data() {
    return {
      currentTime: ""
    };
  },
  mounted() {
    this.updateTime();
    setInterval(this.updateTime, 1000); // Actualizar cada segundo
  },
  methods: {
    updateTime() {
      const timeZone = "GMT-6"; // Zona horaria GMT-6
      const now = moment().tz(timeZone).format("HH:mm:ss");
      this.currentTime = now;
    }
  }
};
</script>