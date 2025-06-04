<template>
  <div class="max-w-4xl mx-auto">
    <div class="bg-white rounded-lg shadow-lg p-6 md:p-8">
      <h1 class="text-2xl md:text-3xl font-bold text-gray-900 mb-4">Welcome to My Nuxt App</h1>
      <p class="text-gray-600 text-base md:text-lg leading-relaxed">
        This is a modern, responsive web application built with Nuxt 3 and Tailwind CSS. 
        It features a mobile-first design approach, ensuring a great user experience across all devices.
      </p>
      
      <!-- Features Section -->
      <div class="mt-8 grid grid-cols-1 md:grid-cols-2 gap-6">
        <div class="bg-gray-50 p-4 rounded-lg">
          <h2 class="text-xl font-semibold text-gray-800 mb-2">Responsive Design</h2>
          <p class="text-gray-600">Optimized for all screen sizes, from mobile to desktop.</p>
        </div>
        <div class="bg-gray-50 p-4 rounded-lg">
          <h2 class="text-xl font-semibold text-gray-800 mb-2">Modern UI</h2>
          <p class="text-gray-600">Clean and intuitive interface with smooth animations.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: 'default'
})
</script> 