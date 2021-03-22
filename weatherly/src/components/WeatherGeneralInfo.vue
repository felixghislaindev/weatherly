<template>
  <div>
    <SearchInput @handleDisplayWeather="displayWeather"/>
    <WeatherLocationAndDate />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import SearchInput from "./SearchInput.vue";
import WeatherLocationAndDate from "./WeatherLocationAndDate.vue";

@Options({
   emits: ['handleDisplayWeatherInfo'],
  components: {
    SearchInput,
    WeatherLocationAndDate,
  },
})
export default class WeatherGeneralInfo extends Vue {
//   methods
    displayWeather(poscode:string):void{
        console.log("here")
        this.$emit('handleDisplayWeatherInfo', poscode)
    }
}
</script>

<style lang="scss" scoped></style>
