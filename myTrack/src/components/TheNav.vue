<script setup>
import {ref} from 'vue'
import { ClockIcon, ListBulletIcon, ChartBarIcon } from "@heroicons/vue/24/outline";
import {PAGE_TIMELINE, PAGE_ACTIVITIES, PAGE_PROGRESS} from '../constants';
import NavItem from "./NavItem.vue";
const navItems = {
    [PAGE_TIMELINE]: ClockIcon,
    [PAGE_ACTIVITIES]: ListBulletIcon,
    [PAGE_PROGRESS]: ChartBarIcon
}

const currentPage = ref(window.location.hash.slice(1))

</script>
<template>
      <nav class="sticky bottom-0 z-10 bg-white">
    <ul class="flex items-center justify-around border-t">
      <NavItem v-for="icon, page in navItems"
      :key="page"
      :href="`#${page}`"
      :class="{'bg-gray-200 pointer-events-none': page == currentPage}"
      @click="currentPage = page"
      >
        <component :is="icon" class="w-6 h-6" /> {{ page }}
      </NavItem>
    </ul>
  </nav>
</template>