<template>
  <div class="wrapper">
    <PageHeader title="test" />
    <TaskList :tasks="tasks" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import PageHeader from './components/PageHeader.vue';
import TaskList, { type Task } from './components/TaskList.vue'

export default defineComponent({
  name: 'App',
  components: {
    PageHeader,
    TaskList
  },
  data() {
    return {
      tasks: [] as Task[]
    };
  },
  created() {
    this.tasks.push(
      {
        id: 1,
        text: 'drs appointment',
        day: 'March 1st at 2pm',
        reminder: true
      },
      {
        id: 2,
        text: 'Resting',
        day: 'Jun 2nd at 5pm',
        reminder: false
      },
    );
  }
});
</script>

<style scoped></style>
