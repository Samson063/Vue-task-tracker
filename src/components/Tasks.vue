<template>
  <div v-for="task in tasks" :key="task.id">
    <Task @delete-task="$emit('delete-task', task.id)" :task="task" />
  </div>
</template>

<script>
import Task from './Task.vue'
export default {
  name: 'taskS',
  props: {
    tasks: Array,
  },
  components: {
    Task,
  },
  emits: ['delete-task'],
}
</script>
