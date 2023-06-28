<script setup>
defineProps({
  items: {
    type: String,
    default: ''
  },
})
</script>

<template>
  <ul class="uk-list uk-list-collapse">
    <li v-for="(item, index) in  items " :key="index">
      {{ item }}
    </li>
  </ul>
</template>