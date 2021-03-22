<template>
  <div class="weather-info">
    <h1 class="title">Weather Details</h1>
    <div class="weather-details">
      <span class="weather-propety">test</span>
      <span class="weather-data">test</span>
    </div>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
  props: {
    weatherInfo: Object,
  },
})
export default class WeatherInDepthInfo extends Vue {
  msg!: string;
}
</script>

<style scoped>
.weather-info {
  text-align: center;
}
.weather-details {
  display: flex;
  justify-content: space-evenly;
}
.weather-data,
.weather-propety {
  font-size: 1rem;
}
</style>
