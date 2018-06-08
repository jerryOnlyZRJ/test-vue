<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <span>count: {{ count }}</span>
    <button @click="addCount">add count</button>
    <button @click="consoleThis">console this</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data: () => {
    return {
      count: 0
    }
  },
  methods: {
    // 不能使用箭头函数，this指向会出现偏差
    addCount: function(){
      this.count++
    },
    consoleThis: () => {
      console.log(this) //undefined
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
