<template>
    <div>
        <h2 class="weather-location"></h2>
        <span class="weather-date-time"></span>
    </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
  props: {
  },
})
export default class WeatherLocationAndDate extends Vue {
  msg!: string;
}
</script>

<style lang="scss" scoped>

</style>