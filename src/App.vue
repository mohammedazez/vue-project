<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
     <!-- <Diskusi4 /> -->
     <tugas2_nomor1 :Alas="20" :Tinggi="10" :Setengah="2"/>
  </div>
</template>

<script>
// import Diskusi4 from './components/Diskusi4.vue'
import tugas2_nomor1 from './components/tugas2_nomor1.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    // Diskusi4,
    tugas2_nomor1
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
