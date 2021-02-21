<template>
  <div id="app">
    
    <GeneratePassword />
  </div>
</template>

<script>
import GeneratePassword from './components/GeneratePassword.vue'

export default {
  name: 'App',
  components: {
    GeneratePassword
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
