<template>
  <div id="app">
    <img src="./assets/logo.png">
   <Users/>
  </div>
</template>

<script>
import Test from './components/Test'
import Users from './components/Users'

export default {
  name: 'App',
  components: {
    Test, Users
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
