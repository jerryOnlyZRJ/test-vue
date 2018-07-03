<template>
  <div class="helloworld">
    <h1>Hello World!</h1>
    <p>{{ msg }}</p>
    <img src="../assets/nmkv.jpg">
  </div>
</template>

<script>
export default {
  name: 'app',
  props: ['msg'],
  components: {
    HelloWorld
  }
}
</script>

<style>
  .helloworld {
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
