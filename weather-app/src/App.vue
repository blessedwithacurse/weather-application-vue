<template>
<div>
  <Header title="Weather App"/>
  <Measurements :measurements="measurements"/>
</div>
</template>

<script>

import Header from './components/Header.vue';
import Measurements from './components/Measurements.vue';

export default {
  name: 'App',
  components: { 
    Header,
    Measurements
  },
  data() {
    return {
      measurements: []
    }
  },
  created() {
    this.measurements = [
      {
        id: 1,
        temp: 18,
        humidity: 12,
      },
       {
        id: 2,
        temp: 34,
        humidity: 80,
      },
      {
        id: 3,
        temp: -7,
        humidity: 3,
      },
    ]
  }
}
</script> 
