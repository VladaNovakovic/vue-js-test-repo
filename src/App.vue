<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <StatusForm msg="This is input form"/>
    <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import StatusForm from './components/StatusForm.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    StatusForm,
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
