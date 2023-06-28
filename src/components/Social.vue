<script setup>
defineProps({
  github: {
    type: String,
    default: ''
  },
  linkedin: {
    type: String,
    default: ''
  },
  twitter: {
    type: String,
    default: ''
  },
  email: {
    type: String,
    default: 'ivan@milincic.com'
  }
})

let size = '28'
</script>

<template>
  <div class="social-links uk-flex uk-flex-middle">

    <a :href="('mailto:' + email)" class="uk-margin-left" :title="email">
      <img src="/svg/mail-bolt.svg" uk-svg :width="size" :height="size" />
    </a>

    <a v-if="github != ''" :href="github" class="uk-margin-left" title="Github" target="_blank" rel="nofollow noreferrer">
      <img src="/svg/github.svg" uk-svg :width="size" :height="size" />
    </a>

    <a v-if="linkedin != ''" :href="linkedin" class="uk-margin-left" title="Linkedin" target="_blank"
      rel="nofollow noreferrer">
      <img src="/svg/linkedin.svg" uk-svg :width="size" :height="size" />
    </a>

    <a v-if="twitter != ''" :href="twitter" class="uk-margin-left" title="Twitter" target="_blank"
      rel="nofollow noreferrer">
      <img src="/svg/twitter.svg" uk-svg :width="size" :height="size" />
    </a>

  </div>
</template>