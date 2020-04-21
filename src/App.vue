<template>
  <div id="app">
    <BodyFat/>
  </div>
</template>

<script>
// inbody data import
// import body_data from '../public/static/data'

// import cart
import BodyFat from "@/components/BodyFat.vue"

export default {
  name: "App",
  components: {
    BodyFat
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
