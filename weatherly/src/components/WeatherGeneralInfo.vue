<template>
    <div>
        <SearchInput/>
        <WeatherLocationAndDate/>
    </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import SearchInput from './SearchInput.vue'
import WeatherLocationAndDate from './WeatherLocationAndDate.vue'

@Options({
  props: {
    msg: String,
  },
  components: {
      SearchInput,
      WeatherLocationAndDate
  },
})
export default class WeatherGeneralInfo extends Vue {
  msg!: string;
}
</script>

<style lang="scss" scoped>

</style>