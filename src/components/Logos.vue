<script setup>
const logos = [
  "processwire",
  "wordpress",
  "woocommerce",
  "php",
  "astro",
  "cloudflare",
  "css",
  "js",
  "less",
  "sass",
  "uikit",
  "copilot",
  "github",
  "laragon",
  "runcloud",
  "vscode",
];
</script>

<template>
  <div class="uk-grid uk-child-width-auto uk-grid-large uk-flex-center" uk-grid>
    <div v-for="(logo, index) in  logos " :key="index">
      <img :src="('/logos/' + logo + '.png')" />
    </div>
  </div>
</template>

<style lang="less" scoped>
img {
  width: auto;
  height: 42px;
  opacity: 0.4;
  transition: all .3s;

  &:hover {
    opacity: 1;
    transition: all .3s;
  }
}
</style>