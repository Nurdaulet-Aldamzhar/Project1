<template>
  <div class="min-h-screen bg-gray-100">
    <!-- Header -->
    <header class="bg-white shadow-md">
      <nav class="container mx-auto px-4 py-4">
        <div class="flex justify-between items-center">
          <!-- Logo -->
          <div class="flex items-center">
            <img src="/logo.png" alt="Logo" class="h-10 w-10 mr-2">
            <span class="text-xl font-bold text-gray-800">My Nuxt App</span>
          </div>

          <!-- Desktop Navigation -->
          <div class="hidden md:flex space-x-6">
            <NuxtLink to="/" class="text-gray-600 hover:text-gray-900">Home</NuxtLink>
            <NuxtLink to="/lab3" class="text-gray-600 hover:text-gray-900">Lab3</NuxtLink>
            <NuxtLink to="/login" class="text-gray-600 hover:text-gray-900">LogIn</NuxtLink>
            <button class="text-gray-600 hover:text-gray-900">LogOut</button>
          </div>

          <!-- Mobile Menu Button -->
          <button @click="isMenuOpen = !isMenuOpen" class="md:hidden">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path v-if="!isMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
              <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>

        <!-- Mobile Navigation -->
        <div v-show="isMenuOpen" class="md:hidden mt-4">
          <div class="flex flex-col space-y-4">
            <NuxtLink to="/" class="text-gray-600 hover:text-gray-900">Home</NuxtLink>
            <NuxtLink to="/lab3" class="text-gray-600 hover:text-gray-900">Lab3</NuxtLink>
            <NuxtLink to="/login" class="text-gray-600 hover:text-gray-900">LogIn</NuxtLink>
            <button class="text-gray-600 hover:text-gray-900">LogOut</button>
          </div>
        </div>
      </nav>
    </header>

    <!-- Main Content -->
    <main class="container mx-auto px-4 py-8">
      <slot />
    </main>
  </div>
</template>

<script setup>
const isMenuOpen = ref(false)
</script> 