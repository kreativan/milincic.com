<script setup>
import Social from './Social.vue';

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
  }
})
</script>

<template>
  <nav id="navbar" class="uk-navbar-container">
    <div class="uk-container uk-container-expand">

      <div class="uk-navbar" uk-navbar>


        <div class="uk-navbar-left">
          <img src="/images/ivan-milincic-logo-white.png" alt="Logo" width="40" height="40" />
        </div>

        <div class="uk-navbar-center">

        </div>

        <div class="uk-navbar-right">
          <Social :github="github" :linkedin="linkedin" :twitter="twitter" />
        </div>

      </div>

    </div>
  </nav>
</template>

<style>
#navbar {
  position: relative;
  padding-top: 30px;
  background: translarent;
}
</style>