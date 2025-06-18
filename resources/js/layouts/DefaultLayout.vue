<script setup>
import Header from '@/Components/Header.vue'
</script>

<template>
  <div class="min-h-screen bg-white dark:bg-gray-900 text-gray-900 dark:text-gray-100">
    <Header />
    <main>
      <slot />
    </main>
  </div>
</template>
