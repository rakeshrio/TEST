<template>
  <div id="app">
        <navigation></navigation>

    <Home></Home>
  </div>
</template>

<script>
import Home from './components/home'
import navigation from './components/navigation'

export default {
  name: 'app',
  components: {
    Home,
    navigation
  }
}
</script>

<style scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
