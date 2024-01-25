<template>
  <button @click="onClick()" :style="{ background: color }" class="custom-button">{{ text }}</button>
</template>

<script lang="ts">
export default {
  name: 'CustomButton',
  props: {
    text: String,
    color: String
  },
  methods: {
    onClick() {
      console.log('button being clicked')
    }
  }
}
</script>

<style scoped>
.custom-button {
  padding: 20px;
}
</style>
