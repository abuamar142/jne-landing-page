<template>
  <header class="bg-white shadow-lg fixed w-full top-0 z-50 transition-all duration-300">
    <div class="container mx-auto px-4 lg:px-8">
      <div class="flex justify-between items-center py-4">
        <!-- Logo -->
        <div class="flex items-center space-x-3">
          <div class="w-10 h-10 bg-gradient-to-r from-blue-600 to-blue-700 rounded-lg flex items-center justify-center">
            <span class="text-white font-bold text-xl">J</span>
          </div>
          <div>
            <h1 class="text-2xl font-bold text-gray-800">JNE</h1>
            <p class="text-xs text-gray-500">Express Delivery</p>
          </div>
        </div>

        <!-- Desktop Navigation -->
        <nav class="hidden md:flex items-center space-x-8">
          <router-link to="/" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">
            Beranda
          </router-link>
          <a href="#services" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">
            Layanan
          </a>
          <router-link to="/about" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">
            Tentang Kami
          </router-link>
          <a href="#contact" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">
            Kontak
          </a>
          <a href="#track" class="bg-gradient-to-r from-blue-600 to-blue-700 text-white px-6 py-2 rounded-full font-semibold hover:from-blue-700 hover:to-blue-800 transition-all duration-300 shadow-md hover:shadow-lg">
            Lacak Kiriman
          </a>
        </nav>

        <!-- Mobile Menu Button -->
        <button @click="toggleMobileMenu" class="md:hidden p-2 rounded-lg hover:bg-gray-100">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
          </svg>
        </button>
      </div>

      <!-- Mobile Navigation -->
      <div v-if="isMobileMenuOpen" class="md:hidden py-4 border-t border-gray-200">
        <nav class="flex flex-col space-y-4">
          <router-link to="/" class="text-gray-700 hover:text-blue-600 font-medium py-2">
            Beranda
          </router-link>
          <a href="#services" class="text-gray-700 hover:text-blue-600 font-medium py-2">
            Layanan
          </a>
          <router-link to="/about" class="text-gray-700 hover:text-blue-600 font-medium py-2">
            Tentang Kami
          </router-link>
          <a href="#contact" class="text-gray-700 hover:text-blue-600 font-medium py-2">
            Kontak
          </a>
          <a href="#track" class="bg-gradient-to-r from-blue-600 to-blue-700 text-white px-6 py-3 rounded-full font-semibold text-center">
            Lacak Kiriman
          </a>
        </nav>
      </div>
    </div>
  </header>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const isMobileMenuOpen = ref(false)

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}
</script>
