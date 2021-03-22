<template>
  <div>
    <h2 class="weather-location">{{currenWeather}}</h2>
    <span class="weather-date-time"></span>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import { reactive } from 'vue'


@Options({
  props: {
    currenWeatherInfo: Object,
  },
   watch: {
    currenWeatherInfo(val) {
        this.currenWeather = reactive(val[0])
    }
  }
})
export default class WeatherLocationAndDate extends Vue {
  currenWeather: Array<any>=[];
}
</script>

<style lang="scss" scoped></style>
