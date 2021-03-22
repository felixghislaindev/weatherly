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
    props: {
        
    },
  components: {
    SearchInput,
    WeatherLocationAndDate,
  },
})
export default class WeatherGeneralInfo extends Vue {
//   methods
    displayWeather(poscode:string):string{
        return poscode
    }
}
</script>

<style lang="scss" scoped></style>
