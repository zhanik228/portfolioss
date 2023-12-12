<script setup>
import { RouterLink, RouterView } from 'vue-router'
import PrimaryHeader from './components/header/PrimaryHeader.vue'
import { onMounted } from 'vue';

onMounted(() => {
  if (!localStorage.getItem('lang')) {
    localStorage.setItem('lang', 'ru')
    window.location.reload()
  }
})
</script>

<template>
  <primary-header />

  <RouterView />
</template>

<style scoped>

</style>
