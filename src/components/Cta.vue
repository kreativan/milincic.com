<script setup>
defineProps({
  email: {
    type: String,
    required: true,
    default: ''
  }
})
</script>

<template>
  <div id="cta">
    <h2 class="uk-heading-small">
      Let’s work together <br />
      on your next project.
    </h2>
    <div class="uk-margin-large-top">
      <p class="uk-text-emphasis uk-text-bold uk-text-uppercase tm-font-base uk-margin-small">
        Write To:
      </p>
      <a class="uk-text-emphasis uk-text-large" :href="('mailto:' + email)">{{ email }}</a>
    </div>
  </div>
</template>
