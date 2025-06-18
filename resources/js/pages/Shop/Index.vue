<template>
  <div class="min-h-screen bg-white dark:bg-gray-900 text-gray-900 dark:text-gray-100">
    <!-- Header -->
    <header class="bg-gray-100 dark:bg-gray-900 shadow-md p-4 flex justify-between items-center">
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

    <!-- Контент -->
    <main class="p-8">
      <h1 class="text-3xl font-bold mb-6">Добро пожаловать в наш магазин</h1>

      <table class="w-full table-auto border-collapse border border-gray-300 dark:border-gray-700 shadow-md">
        <thead class="bg-gray-100 dark:bg-gray-800">
          <tr>
            <th class="border p-2">ID</th>
            <th class="border p-2">Название</th>
            <th class="border p-2">Описание</th>
            <th class="border p-2">Цена</th>
            <th class="border p-2">Кол-во</th>
          </tr>
        </thead>
        <tbody>
          <tr
            v-for="product in products"
            :key="product.id"
            class="hover:bg-gray-50 dark:hover:bg-gray-800"
          >
            <td class="border p-2 text-center">{{ product.id }}</td>
            <td class="border p-2">{{ product.name }}</td>
            <td class="border p-2">{{ product.description }}</td>
            <td class="border p-2">{{ product.price }} сом</td>
            <td class="border p-2 text-center">{{ product.quantity }}</td>
          </tr>
        </tbody>
      </table>

      <div v-if="products.length === 0" class="mt-6 text-gray-500 dark:text-gray-400">
        Пока нет товаров для отображения.
      </div>
    </main>
  </div>
</template>

<script setup>
import { Link as InertiaLink } from '@inertiajs/vue3'

defineProps({
  products: Array
})
</script>
