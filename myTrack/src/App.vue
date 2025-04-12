<script setup>
import { ref } from 'vue';
import TheHeader from './components/TheHeader.vue';
import TheNav from './components/TheNav.vue'
const input = ref('')
</script>

<template>
  <TheHeader />
  <main class="flex flex-grow flex-col items-center">
    <input type="text" class="bg-gray-200 w-10" v-model="input" />
    <p>{{ input }}</p>
  </main>
  <TheNav />
  </template>
<style scoped>
</style>
