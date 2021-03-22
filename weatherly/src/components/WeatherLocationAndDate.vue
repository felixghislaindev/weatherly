<template>
  <div>
    <h2 class="weather-location">{{currenWeather.name}}</h2>
    <span class="weather-date-time">{{weatherInCelcius}}&#8451;</span>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import { reactive } from 'vue'

interface WeatherInfo {
  id: string
  country: string
  coord: {
    lon: number,
    lat: number
  }
  main:{
    temp:number
  }
}

@Options({
  props: {
    currenWeatherInfo: Array
  },
   watch: {
    // currenWeatherInfo(val) {
    //     this.currenWeather = val
    // }
  }
})
export default class WeatherLocationAndDate extends Vue {
  // currenWeather: Array<WeatherInfo>;
  get weatherInCelcius(){
    return this.currenWeather
  }
}
</script>

<style lang="scss" scoped></style>
