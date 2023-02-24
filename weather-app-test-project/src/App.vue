<template>
  <div id="app">
    <NavBar/>
    <Select/>
  </div>
</template>

<script lang='ts'>
import { defineComponent } from 'vue'
import NavBar from './components/NavBar.vue'
import Select from './components/Select.vue';
import WeatherCard from './components/WeatherCard.vue';

export default defineComponent({
  name: 'App',
  components: {
    NavBar,
    Select,
    WeatherCard
  },
 
})  
</script> 


