<template>
  <header class="bg-gray-100 dark:bg-gray-900 text-gray-900 dark:text-gray-100 shadow-md p-4 flex justify-between items-center">
    <div class="text-2xl font-bold">
      <a href="/" class="hover:underline">Мой Магазин</a>
    </div>

    <nav>
      <ul class="flex space-x-6">
        <li>
          <inertia-link href="/" class="hover:text-blue-600 dark:hover:text-blue-400">Главная</inertia-link>
        </li>
        <li>
          <inertia-link href="/shop" class="hover:text-blue-600 dark:hover:text-blue-400">Магазин</inertia-link>
        </li>
        <li>
          <inertia-link href="/about" class="hover:text-blue-600 dark:hover:text-blue-400">О нас</inertia-link>
        </li>
        <li>
          <inertia-link href="/contact" class="hover:text-blue-600 dark:hover:text-blue-400">Контакты</inertia-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script setup>
import { Link as InertiaLink } from '@inertiajs/vue3'
</script>
