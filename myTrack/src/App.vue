<script setup>
import { CheckCircleIcon } from "@heroicons/vue/24/solid";
</script>

<template>
  <header class="sticky item-center justify-between border-b bg-white p-3">
    <a href="#">
      <img src="./assets/logo.png" alt="Logo" class="h-20">
    </a>

    <a href="#" class="text-sm">
      <div v-if="true" class="flex item-center gap-1">
        Day complete!
        <CheckCircleIcon class="h-7 text-green-500" />
      </div>

      <div v-else class="flex item-center gap-1">
        <div>Progress: <span class="font-mono">20%</span></div>
        <div class="h-3 w-3 rounded-full bg-red-500"></div>
      </div>

    </a>
  </header>

  <main>
    
  </main>

  </template>

<style scoped>
header{
  top: 0;
  z-index: 20;
  display: flex;
  height: 5;
}
</style>
