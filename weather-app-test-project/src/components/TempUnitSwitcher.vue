<template>
  <div>
    <button @click="$emit('convertTemp')">
      Switch to Fahrenheit
    </button>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'TempUnitSwitcher',
  emits: ['convertTemp'],
  props: {
    temp: Number,
    fahrenheit: String,
    celcius: String
  },
  setup(props, { emit })  {
    // const convertedTemp = ref(0)
    // const switchUnit = (temp: any) => {
    //   convertedTemp.value = Math.round(temp * (9 / 5) + 32)
    // }
    emit('convertTemp')
  }
})
</script>

<style lang="scss">
</style>


