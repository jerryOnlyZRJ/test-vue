<template>
  <div class="page-index">
    <Helloworld />
    这是index页面。
    <TestStyle />
  </div>
</template>

<script>
import Helloworld from '../../components/Helloworld/index.vue'
import TestStyle from '../../components/TestStyle/index.vue'

export default {
  name: 'Index',
  components: {
    Helloworld,
    TestStyle
  }
}
</script>

<style scoped></style>
