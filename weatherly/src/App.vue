<template>
  <w-app>
    <w-flex>
      <div class="xs5 pa1">
        <div class="weather-general-info py3">
          <h2 class="title">Weatherly.</h2>
          <WeatherGeneralInfo />
          <h3>16<span>&#8451;</span></h3>
        </div>
      </div>
      <div class="xs7 pa1">
        <div class="weather-in-depth-info py3">
          <WeatherInDepthInfo />
        </div>
      </div>
    </w-flex>
  </w-app>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import WeatherGeneralInfo from "./components/WeatherGeneralInfo.vue";
import WeatherInDepthInfo from "./components/WeatherInDepthInfo.vue";

@Options({
  components: {
    WeatherGeneralInfo,
    WeatherInDepthInfo,
  },
})
export default class App extends Vue {}
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Roboto:300,400,500");
#app {
  color: #2c3e50;
  margin: 20px;
}
body {
  font-family: Roboto;
  font-weight: 400;
  width: 100%;
  margin: 0;
  font-size: 1.6rem;
  background-color: #7daadf;
}
.weather-general-info,
.weather-in-depth-info {
  background-color: #fff;
  border-radius: 10px;
  padding: 20px;
}
.title {
  font-size: 1rem;
}
</style>
