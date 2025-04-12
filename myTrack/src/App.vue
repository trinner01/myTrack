<script setup>
import { ref } from 'vue';
import TheHeader from './components/TheHeader.vue';
import TheNav from './components/TheNav.vue';

const firstName = ref('');
const lastName = ref('');
const cards = ref([]);

function save() {
  if (firstName.value && lastName.value) {
    cards.value.push(`${firstName.value} ${lastName.value}`);
    console.log('Save clicked:', cards.value);
    firstName.value = '';
    lastName.value = '';
  }
}
</script>

<template>
  <TheHeader />
  <main class="flex flex-grow flex-col">
    <button @click="save">Save</button>
    firstName:<input type="text" class="bg-gray-200 w-20" v-model="firstName" />
    lastName:<input type="text" class="bg-gray-200 w-20" v-model="lastName" />
    <p>{{ firstName }}</p>
    <p>{{ lastName }}</p>
    <br>
    <h1>Cards:</h1>
    <ul>
      <li v-for="(card, index) in cards" :key="index">{{ card }}</li>
    </ul>
  </main>
  <TheNav />
</template>

<style scoped>
</style>