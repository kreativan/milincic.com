<script setup>
defineProps({
  items: {
    type: Array,
    required: true,
    default: []
  },
  open: {
    type: Boolean,
    required: false,
    default: false
  }
})
</script>

<template>
  <ul class="uk-accordion" uk-accordion>
    <li v-for="(item, index) in items" :key="index" :class="(open ? 'uk-open' : '')">
      <a class="uk-accordion-title" href="#">
        <h4 class="uk-margin-remove tm-font-base uk-text-uppercase uk-text-bold">
          {{ item.title }}
        </h4>
        <span v-if="item.subtitle" class="uk-display-block uk-text-small uk-text-muted">
          {{ item.subtitle }}
        </span>
      </a>
      <div class="uk-accordion-content">
        <div class="uk-background-muted uk-padding">
          {{ item.description ? item.description : item.text }}
        </div>
      </div>
    </li>
  </ul>
</template>

<style>
.uk-accordion-title>span {
  margin-top: 5px;
}
</style>