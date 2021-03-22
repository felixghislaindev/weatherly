<template>
  <div>
    <w-input
      class="mb2"
      label="Enter your postcode"
      label-position="inside"
      outline
      inner-icon-left="wi-search"
      @blur="setPostCode"
    >
    </w-input>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
    emits: ['handleDisplayWeather']
})
export default class SearchInput extends Vue {
  poscode:string|undefined
  errorMsgstring:string|undefined
//   computed
  setPostCode(e):void{
      const value = e.target.value
      const validPostcodeRegex = /^([A-Z]{1,2}\d[A-Z\d]? ?\d[A-Z]{2}|GIR ?0A{2})$/gmi
      if(validPostcodeRegex.test(value)){
          this.poscode = value
          this.$emit('handleDisplayWeather',this.poscode)
      } else{
      this.errorMsgstring = 'please enter a valid postcode'

      }
  }
}
</script>

<style lang="scss" scoped></style>
