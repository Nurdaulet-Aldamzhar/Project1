<template>
  <div class="container mx-auto px-4 py-8">
    <h1 class="text-4xl font-bold text-center mb-12">Наша Команда</h1>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      <!-- Адлет -->
      <div class="bg-white rounded-lg shadow-lg p-6 text-center transform transition duration-300 hover:scale-105 hover:shadow-xl">
        <h2 class="text-2xl font-semibold text-gray-800 mb-2">Адлет</h2>
        <p class="text-gray-600">Амбициозный парень с хорошими лидерскими качествами</p>
      </div>

      <!-- Нурдаулет -->
      <div class="bg-white rounded-lg shadow-lg p-6 text-center transform transition duration-300 hover:scale-105 hover:shadow-xl">
        <h2 class="text-2xl font-semibold text-gray-800 mb-2">Нурдаулет</h2>
        <p class="text-gray-600">Ответственный за команду, который готов помочь каждому</p>
      </div>

      <!-- Ералы -->
      <div class="bg-white rounded-lg shadow-lg p-6 text-center transform transition duration-300 hover:scale-105 hover:shadow-xl">
        <h2 class="text-2xl font-semibold text-gray-800 mb-2">Ералы</h2>
        <p class="text-gray-600">Сдержанный, но в тоже время очень умный парень</p>
      </div>

      <!-- Амина -->
      <div class="bg-white rounded-lg shadow-lg p-6 text-center transform transition duration-300 hover:scale-105 hover:shadow-xl">
        <h2 class="text-2xl font-semibold text-gray-800 mb-2">Амина</h2>
        <p class="text-gray-600">Жизнерадостная девушка, поднимает настроение всей команды</p>
      </div>

      <!-- Аружан -->
      <div class="bg-white rounded-lg shadow-lg p-6 text-center transform transition duration-300 hover:scale-105 hover:shadow-xl">
        <h2 class="text-2xl font-semibold text-gray-800 mb-2">Аружан</h2>
        <p class="text-gray-600">Сердце команды</p>
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: 'default'
})

// Placeholder images - replace with actual member photos if available
// Ensure actual images are placed in the public directory (e.g., public/images/team/)
</script>

<style scoped>
/* Add any specific styles for the team page if needed */
</style> 