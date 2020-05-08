<template>
  <div id="app">
    <BodyWeight :bodyDatas="bodyDatas"/>
    <BodyFatWeight :bodyDatas="bodyDatas"/>
    <PercentBodyFat :bodyDatas="bodyDatas"/>
    <SkeletalMuscleMass :bodyDatas="bodyDatas"/>
  </div>
</template>

<script>
// inbody data import
import body_data from '../public/static/data'

// import cart
import BodyWeight from "@/components/BodyWeight.vue"
import SkeletalMuscleMass from "@/components/SkeletalMuscleMass.vue"
import BodyFatWeight from "@/components/BodyFatWeight.vue"
import PercentBodyFat from "@/components/PercentBodyFat.vue"

export default {
  name: "App",
  components: {
    BodyWeight,
    SkeletalMuscleMass,
    BodyFatWeight,
    PercentBodyFat
  },
  data () {
    return {
      bodyDatas: body_data
    }
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
