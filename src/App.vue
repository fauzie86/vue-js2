<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Task1 msg="Welcome to Your Vue.js App"/>

  
</template>

<script>
import Task1 from './components/Task1.vue';



export default {
  name: 'App',
  components: {
    Task1,
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

