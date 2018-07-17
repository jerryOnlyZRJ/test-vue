<template>
  <div id="app">
    <!-- <img src="./assets/nmkv.jpg"> -->
    <HelloWorld></HelloWorld>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import DropMenu from './components/DropMenu/DropMenu.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    DropMenu
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
