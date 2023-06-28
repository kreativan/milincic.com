<script setup>
defineProps({
  items: {
    type: Array,
    required: true,
    default: []
  },
})
</script>

<template>
  <p v-for="(item, index) in items" :key="index">{{ item.text }}</p>
</template>