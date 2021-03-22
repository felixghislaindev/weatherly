<template>
  <div>
    <SearchInput @handleDisplayWeather="displayWeather"/>
    <WeatherLocationAndDate  :currenWeatherInfo="currenWeatherInfo"/>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import SearchInput from "./SearchInput.vue";
import WeatherLocationAndDate from "./WeatherLocationAndDate.vue";
import { reactive } from 'vue'

@Options({
   emits: ['handleDisplayWeatherInfo'],
   props: {
    weatherInfo: Object,
  },
  components: {
    SearchInput,
    WeatherLocationAndDate,
  },
   watch: {
    weatherInfo(val) {
        this.currenWeatherInfo = reactive(val[0])
    }
  }
})
export default class WeatherGeneralInfo extends Vue {
//   data
  currenWeatherInfo:Array<any>=[];
    //   methods
    displayWeather(poscode:string):void{
        this.$emit('handleDisplayWeatherInfo', poscode)
    }
}
</script>

<style lang="scss" scoped></style>
