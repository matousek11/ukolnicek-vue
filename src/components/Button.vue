<script setup lang="ts">
defineProps<{
  text: string
  color: string
}>()
</script>

<template>
  <p class="button" @click="$emit('on-press-function')">{{ text }}</p>
</template>

<style scoped>
.button {
  color: white;
  background-color: v-bind(color);
  border: 2px solid v-bind(color);
  margin: 2px 4px;
  padding: 3px 8px;
  border-radius: 4px;
  cursor: pointer;
}
.button:hover {
  color: v-bind(color);
  background-color: white;
  border: 2px solid v-bind(color);
}
</style>
