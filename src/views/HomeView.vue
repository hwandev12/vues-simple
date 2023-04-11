<template>
  <div class="home">
    <Task task="Task Comp" />
  </div>
</template>

<script>
import Task from '../components/Task.vue'
export default {
  name: 'HomeView',
  components: {
    Task
  }
}
</script>

<style scoped>
.container {
  max-width: 1250px;
  margin-left: auto;
  margin-right: auto;
  padding: 0 20px;
}
</style>
