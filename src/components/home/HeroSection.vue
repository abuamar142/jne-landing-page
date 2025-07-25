<template>
  <section class="relative min-h-screen flex items-center justify-center overflow-hidden">
    <!-- Background Gradient -->
    <div class="absolute inset-0 bg-gradient-to-br from-blue-50 via-white to-blue-50"></div>

    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-5">
      <div class="absolute inset-0 bg-gradient-to-r from-blue-600 to-blue-700"></div>
    </div>

    <div class="relative z-10 container mx-auto px-4 lg:px-8 pt-20">
      <div class="grid lg:grid-cols-2 gap-12 items-center">
        <!-- Content -->
        <div class="text-center lg:text-left">
          <div class="inline-flex items-center bg-blue-100 text-blue-600 px-4 py-2 rounded-full text-sm font-semibold mb-6">
            <svg class="w-4 h-4 mr-2 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path>
            </svg>
            Terpercaya Sejak 1990
          </div>

          <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
            Solusi Pengiriman
            <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-600 to-blue-700">
              Terdepan
            </span>
            di Indonesia
          </h1>

          <p class="text-lg md:text-xl text-gray-600 mb-8 leading-relaxed max-w-2xl">
            Mengantarkan lebih dari 10 juta paket setiap tahun dengan jangkauan ke seluruh pelosok Indonesia.
            Kepercayaan Anda adalah prioritas utama kami.
          </p>

          <!-- CTA Buttons -->
          <div class="flex flex-col sm:flex-row gap-4 mb-12">
            <a href="#track" class="bg-gradient-to-r from-blue-600 to-blue-700 text-white px-8 py-4 rounded-full font-semibold text-lg hover:from-blue-700 hover:to-blue-800 transition-all duration-300 shadow-xl hover:shadow-2xl transform hover:-translate-y-1">
              <svg class="w-5 h-5 inline mr-2 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z" clip-rule="evenodd"></path>
              </svg>
              Lacak Kiriman
            </a>
            <a href="#services" class="border-2 border-gray-300 text-gray-700 px-8 py-4 rounded-full font-semibold text-lg hover:border-blue-600 hover:text-blue-600 transition-all duration-300">
              Jelajahi Layanan
            </a>
          </div>

          <!-- Stats -->
          <div class="grid grid-cols-3 gap-8 text-center">
            <div>
              <div class="text-2xl md:text-3xl font-bold text-gray-900 mb-1">35+</div>
              <div class="text-sm text-gray-600">Tahun Pengalaman</div>
            </div>
            <div>
              <div class="text-2xl md:text-3xl font-bold text-gray-900 mb-1">500+</div>
              <div class="text-sm text-gray-600">Kota Terjangkau</div>
            </div>
            <div>
              <div class="text-2xl md:text-3xl font-bold text-gray-900 mb-1">10M+</div>
              <div class="text-sm text-gray-600">Paket Terkirim</div>
            </div>
          </div>
        </div>

        <!-- Image/Illustration -->
        <div class="hidden lg:block">
          <div class="relative">
            <!-- Main illustration -->
            <div class="w-full h-96 bg-gradient-to-br from-blue-100 to-blue-200 rounded-3xl flex items-center justify-center shadow-2xl transform rotate-3 hover:rotate-1 transition-transform duration-500">
              <div class="text-center">
                <div class="w-32 h-32 bg-white rounded-full flex items-center justify-center shadow-lg mb-4 mx-auto">
                  <svg class="w-16 h-16 text-blue-600" fill="currentColor" viewBox="0 0 20 20">
                    <path d="M8 16.5a1.5 1.5 0 11-3 0 1.5 1.5 0 013 0zM15 16.5a1.5 1.5 0 11-3 0 1.5 1.5 0 013 0z"></path>
                    <path d="M3 4a1 1 0 00-1 1v1a1 1 0 001 1h1a1 1 0 001-1V5a1 1 0 00-1-1H3zM6 4a1 1 0 000 2v9a1 1 0 001 1h8a1 1 0 001-1V6a1 1 0 100-2H6z"></path>
                  </svg>
                </div>
                <h3 class="text-xl font-bold text-gray-800 mb-2">Delivery Truck</h3>
                <p class="text-gray-600">Siap Melayani 24/7</p>
              </div>
            </div>

            <!-- Floating elements -->
            <div class="absolute -top-6 -right-6 w-24 h-24 bg-yellow-400 rounded-full flex items-center justify-center shadow-lg animate-bounce">
              <svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path>
              </svg>
            </div>

            <div class="absolute -bottom-6 -left-6 w-20 h-20 bg-green-400 rounded-full flex items-center justify-center shadow-lg animate-pulse">
              <svg class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M5 2a1 1 0 011 1v1h1a1 1 0 010 2H6v1a1 1 0 01-2 0V6H3a1 1 0 010-2h1V3a1 1 0 011-1zm0 10a1 1 0 011 1v1h1a1 1 0 110 2H6v1a1 1 0 11-2 0v-1H3a1 1 0 110-2h1v-1a1 1 0 011-1zM12 2a1 1 0 01.967.744L14.146 7.2 17.5 9.134a1 1 0 010 1.732L14.146 12.8l-1.179 4.456a1 1 0 01-1.934 0L9.854 12.8 6.5 10.866a1 1 0 010-1.732L9.854 7.2l1.179-4.456A1 1 0 0112 2z" clip-rule="evenodd"></path>
              </svg>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Scroll indicator -->
    <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce">
      <svg class="w-6 h-6 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
      </svg>
    </div>
  </section>
</template>

<script setup lang="ts">
// Hero section script here if needed
</script>
