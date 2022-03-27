<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <api-page></api-page>
</template>

<script>
import ApiPage from './components/ApiPage.vue'

export default {
  name: 'App',
  components: {
    ApiPage
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
