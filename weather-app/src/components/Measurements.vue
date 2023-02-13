<template>
  <div v-for="measure in measurements">
    <h3>{{ measure.temp }}</h3>
  </div>
</template>

<script>
export default {
  name: 'Measurements',
  props: {
    measurements: Array
  }
}
</script>