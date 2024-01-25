<template>
  <div :key="task.id" v-for="task in tasks">
    <SingleTask :task="task" />
  </div>
</template>

<script  lang="ts">
import SingleTask from './SingleTask.vue'

export interface Task {
  id: number;
  text: string;
  day: string;
  reminder: boolean;
}

export default {
  name: 'TaskList',
  props: {
    tasks: Array as () => Task[]
  },
  components: {
    SingleTask
  }
}
</script>