<template>
  <div class="min-h-screen bg-gray-100" style="background-image: url('/background.png'); background-size: cover; background-position: center;">
    <!-- Header -->
    <header class="bg-white shadow-md fixed w-full top-0 z-50">
      <nav class="container mx-auto px-4 py-4">
        <div class="flex justify-between items-center">
          <!-- Logo -->
          <div class="flex items-center">
            <img src="/logo.png" alt="Logo" class="h-10 w-10 mr-2 rounded-full">
            <span class="text-xl font-bold text-gray-800">Bratva</span>
          </div>

          <!-- Desktop Navigation -->
          <div class="hidden md:flex space-x-6">
            <NuxtLink to="/" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">Home</NuxtLink>
            <NuxtLink to="/login" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">LogIn</NuxtLink>
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

    <!-- Footer -->
    <footer class="bg-white shadow-md mt-8 py-8">
      <div class="container mx-auto px-4 flex flex-col md:flex-row items-center justify-between">
        <div class="flex items-center mb-4 md:mb-0">
          <a href="https://www.instagram.com/kozybayevuniversity?igsh=MXNpMXdjc3J2MHhvYQ==" target="_blank">
            <img src="/manash_kozybayev_north_kazakhstan_university_logo.png" alt="Manash Kozybayev North Kazakhstan University Logo" class="h-12 w-auto mr-4">
          </a>
        </div>

        <div class="flex flex-col md:flex-row items-center space-y-2 md:space-y-0 md:space-x-6 text-gray-600">
          <a href="https://www.instagram.com/zhanga1iyev" target="_blank" class="hover:text-gray-900 transition-colors duration-200 flex items-center">
            <img src="/isnt_logo.png" alt="Instagram Logo" class="h-5 w-5 mr-1">
            Instagram
          </a>
          <a href="https://www.instagram.com/amanzholo1v/" target="_blank" class="hover:text-gray-900 transition-colors duration-200 flex items-center">
             <img src="/isnt_logo.png" alt="Instagram Logo" class="h-5 w-5 mr-1">
            Instagram
          </a>
          <a href="https://www.instagram.com/a1tmukhambet?igsh=MWx1aWllajE3d28xZg==" target="_blank" class="hover:text-gray-900 transition-colors duration-200 flex items-center">
             <img src="/isnt_logo.png" alt="Instagram Logo" class="h-5 w-5 mr-1">
            Instagram
          </a>
          <span class="flex items-center">
             <img src="/phonelogo.png" alt="Phone Logo" class="h-5 w-5 mr-1">
            +7 702 912 7039
          </span>
        </div>
      </div>
    </footer>
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