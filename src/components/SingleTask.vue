<template>
  <h2 v-if="task">{{ task.text }} </h2>
  <p v-if="task">{{ task.day }}</p>

  <div v-else>
    No task available.
  </div>
</template>

<script lang="ts">

export default {
  name: 'SingleTask',
  props: {
    task: Object,
    default: null
  }
}
</script>

<style scoped></style>
