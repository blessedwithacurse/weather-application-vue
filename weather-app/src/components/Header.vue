<template>
  <header>
    <h1>{{ title }}</h1>
    <Button text="Add" color= "green"/>
  </header>
</template>

<script>
import Button from './Button.vue'

export default {
  name: "Header",
  props: {
    title: String
  },
  components: {
    Button
  }
}
</script>

<style scoped> /* scoped means that these styles are only for this component*/
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  
  }
</style>


