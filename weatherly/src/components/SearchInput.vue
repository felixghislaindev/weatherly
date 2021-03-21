<template>
    <div>
        <w-input
  class="mb2"
  label="Enter your postcode"
  label-position="inside"
  outline
  inner-icon-left="wi-search">
</w-input>
    </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
  props: {
    msg: String,
  },
})
export default class SearchInput extends Vue {
  msg!: string;
}
</script>

<style lang="scss" scoped>

</style>