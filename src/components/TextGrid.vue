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
  <div class="uk-grid uk-child-width-1-3@m uk-child-width-1-2@s uk-grid-small uk-grid-match" uk-grid>
    <div v-for="(item, index) in items" :key="index">
      <div class="text-grid-item uk-padding-small uk-border-rounded uk-position-relative">
        <h4 class="uk-margin-remove tm-font-base uk-text-default uk-text-bold">
          {{ item.title }}
        </h4>
        <p v-if="item.subtitle" class="uk-display-block uk-text-small uk-text-muted uk-margin-small">
          {{ item.subtitle }}
        </p>
        <p v-if="item.text">
          {{ item.text }}
        </p>
      </div>
    </div>
  </div>
</template>

<style lang="less">
.text-grid-item:hover {
  background-color: fade(white, 2%);
  transition: all .3s;
}
</style>