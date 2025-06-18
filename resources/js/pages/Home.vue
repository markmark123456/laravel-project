<template>
  <div class="p-6">
    <h1 class="text-2xl font-bold mb-4 text-gray-900 dark:text-white">Vue + Inertia Demo</h1>

    <div class="bg-gray-100 dark:bg-gray-800 p-4 rounded shadow max-w-sm">
      <p class="mb-2 text-gray-900 dark:text-white">
        Счётчик: <strong>{{ count }}</strong>
      </p>

      <div class="flex gap-2">
        <button
          @click="count++"
          class="bg-green-500 hover:bg-green-600 text-white px-4 py-2 rounded"
        >+</button>
        <button
          @click="count--"
          class="bg-red-500 hover:bg-red-600 text-white px-4 py-2 rounded"
        >-</button>
      </div>
    </div>

    <p class="mt-4 text-gray-600 dark:text-gray-400">
      Это пример Vue-компонента, адаптированного под тёмную и светлую тему.
    </p>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const count = ref(0)
</script>
