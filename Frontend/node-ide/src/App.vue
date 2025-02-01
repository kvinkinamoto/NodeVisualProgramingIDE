<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="flex h-screen">
    <!-- Ліва панель -->
    <aside class="w-64 bg-gray-800 text-white p-4">
      <h2 class="text-xl font-bold mb-4">Ліва панель</h2>
      <ul>
        <li class="mb-2"><RouterLink to="/" class="hover:text-gray-400">Головна</RouterLink></li>
        <li><RouterLink to="/about" class="hover:text-gray-400">Про проект</RouterLink></li>
      </ul>
    </aside>

    <!-- Основний контент -->
    <div class="flex-1 flex flex-col">
      <header class="bg-gray-900 text-white p-4 flex justify-between items-center">
        <span class="text-lg font-semibold">Нодова система генерації коду</span>
      </header>

      <main class="flex-1 p-4 bg-gray-700 text-white">
        <RouterView />
      </main>

      <!-- Статус-бар -->
      <footer class="bg-gray-900 text-white p-2 text-center text-sm">
        Статус: Готовий до роботи
      </footer>
    </div>

    <!-- Права панель -->
    <aside class="w-64 bg-gray-800 text-white p-4">
      <h2 class="text-xl font-bold mb-4">Права панель</h2>
      <p>Тут буде додаткова інформація або налаштування</p>
    </aside>
  </div>
</template>

<style scoped>
</style>
