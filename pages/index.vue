<template>
  <div class="min-h-screen bg-gray-100">
    <header class="bg-white shadow">
      <nav class="container mx-auto px-4 py-4">
        <div class="flex justify-between items-center">
          <h1 class="text-2xl font-bold text-gray-800">My Nuxt App</h1>
          <div class="space-x-4">
            <NuxtLink to="/" class="text-gray-600 hover:text-gray-900">Home</NuxtLink>
            <NuxtLink to="/lab3" class="text-gray-600 hover:text-gray-900">Lab 3</NuxtLink>
            <NuxtLink to="/login" class="text-gray-600 hover:text-gray-900">Login</NuxtLink>
          </div>
        </div>
      </nav>
    </header>

    <main class="container mx-auto px-4 py-8">
      <h2 class="text-3xl font-bold text-gray-900 mb-4">Welcome to My Nuxt App</h2>
      <p class="text-gray-600">This is a starter template with Nuxt 3 and Tailwind CSS.</p>
    </main>
  </div>
</template> 