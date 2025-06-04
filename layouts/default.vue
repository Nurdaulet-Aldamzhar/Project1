<template>
  <div class="min-h-screen bg-gray-100">
    <!-- Header -->
    <header class="bg-white shadow-md fixed w-full top-0 z-50">
      <nav class="container mx-auto px-4 py-4">
        <div class="flex justify-between items-center">
          <!-- Logo -->
          <div class="flex items-center">
            <img src="/logo.png" alt="Logo" class="h-10 w-10 mr-2">
            <span class="text-xl font-bold text-gray-800">My Nuxt App</span>
          </div>

          <!-- Desktop Navigation -->
          <div class="hidden md:flex space-x-6">
            <NuxtLink to="/" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">Home</NuxtLink>
            <NuxtLink to="/login" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">LogIn</NuxtLink>
            <button class="text-gray-600 hover:text-gray-900 transition-colors duration-200">LogOut</button>
          </div>

          <!-- Mobile Menu Button -->
          <button @click="isMenuOpen = !isMenuOpen" class="md:hidden focus:outline-none">
            <svg class="w-6 h-6 transition-transform duration-300" :class="{ 'rotate-90': isMenuOpen }" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path v-if="!isMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
              <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>

        <!-- Mobile Navigation -->
        <transition
          enter-active-class="transition duration-200 ease-out"
          enter-from-class="transform scale-95 opacity-0"
          enter-to-class="transform scale-100 opacity-100"
          leave-active-class="transition duration-100 ease-in"
          leave-from-class="transform scale-100 opacity-100"
          leave-to-class="transform scale-95 opacity-0"
        >
          <div v-show="isMenuOpen" class="md:hidden mt-4">
            <div class="flex flex-col space-y-4 bg-white rounded-lg shadow-lg p-4">
              <NuxtLink 
                to="/" 
                class="text-gray-600 hover:text-gray-900 transition-colors duration-200"
                @click="isMenuOpen = false"
              >
                Home
              </NuxtLink>
              <NuxtLink 
                to="/login" 
                class="text-gray-600 hover:text-gray-900 transition-colors duration-200"
                @click="isMenuOpen = false"
              >
                LogIn
              </NuxtLink>
              <button 
                class="text-gray-600 hover:text-gray-900 transition-colors duration-200 text-left"
                @click="isMenuOpen = false"
              >
                LogOut
              </button>
            </div>
          </div>
        </transition>
      </nav>
    </header>

    <!-- Main Content -->
    <main class="container mx-auto px-4 py-8 mt-16">
      <transition
        enter-active-class="transition duration-300 ease-out"
        enter-from-class="transform translate-y-4 opacity-0"
        enter-to-class="transform translate-y-0 opacity-100"
        leave-active-class="transition duration-200 ease-in"
        leave-from-class="transform translate-y-0 opacity-100"
        leave-to-class="transform translate-y-4 opacity-0"
      >
        <slot />
      </transition>
    </main>
  </div>
</template>

<script setup>
const isMenuOpen = ref(false)

// Close menu when clicking outside
onMounted(() => {
  document.addEventListener('click', (e) => {
    const menu = document.querySelector('.md\\:hidden')
    const button = document.querySelector('button.md\\:hidden')
    if (menu && button && !menu.contains(e.target) && !button.contains(e.target)) {
      isMenuOpen.value = false
    }
  })
})
</script>

<style>
/* Add smooth scrolling */
html {
  scroll-behavior: smooth;
}

/* Improve touch targets on mobile */
@media (max-width: 768px) {
  button, a {
    min-height: 44px;
    min-width: 44px;
  }
}
</style> 