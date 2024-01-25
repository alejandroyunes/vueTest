<template>
  <header>
    <h1>{{ title }}</h1>
    <CustomButton text="click me" color="red" />
  </header>
</template>

<script lang="ts">
import CustomButton from './CustomButton.vue';

export default {
  name: 'PageHeader',
  props: {
    title: {
      type: String,
      default: 'This is the default title',
    },
  },
  components: {
    CustomButton,
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: white;
}
</style>