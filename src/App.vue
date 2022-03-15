<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <img :src="imgSrc1" alt="">
    <img :src="imgSrc2" alt="">
  </div>
</template>

<script>
import imgSrc from '../src/assets/logo.png'
export default {
  name: 'App',
  data(){
    return{
      imgSrc1: require('../src/assets/logo.png'),
      imgSrc2: imgSrc
    }
  },
  created(){
    console.log(process.env.VUE_APP_BASE_URL)
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
