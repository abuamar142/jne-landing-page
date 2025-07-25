<template>
  <section id="track" class="py-20 bg-gradient-to-br from-red-600 to-red-700">
    <div class="container mx-auto px-4 lg:px-8">
      <div class="text-center text-white mb-12">
        <h2 class="text-3xl md:text-4xl font-bold mb-4">
          Lacak Kiriman Anda
        </h2>
        <p class="text-xl text-red-100 max-w-2xl mx-auto">
          Pantau status pengiriman real-time dan dapatkan update langsung ke WhatsApp atau email
        </p>
      </div>

      <div class="max-w-2xl mx-auto">
        <!-- Tracking Form -->
        <div class="bg-white rounded-2xl p-8 shadow-2xl">
          <form @submit.prevent="trackPackage" class="space-y-6">
            <div>
              <label for="trackingNumber" class="block text-sm font-semibold text-gray-700 mb-2">
                Nomor Resi
              </label>
              <div class="relative">
                <input
                  id="trackingNumber"
                  v-model="trackingNumber"
                  type="text"
                  placeholder="Masukkan nomor resi (contoh: JNE1234567890)"
                  class="w-full px-4 py-4 border-2 border-gray-200 rounded-xl focus:border-red-500 focus:outline-none transition-colors duration-300 text-lg"
                  required
                />
                <div class="absolute inset-y-0 right-0 pr-4 flex items-center">
                  <svg class="w-5 h-5 text-gray-400" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z" clip-rule="evenodd"></path>
                  </svg>
                </div>
              </div>
            </div>

            <button
              type="submit"
              :disabled="isLoading"
              class="w-full bg-gradient-to-r from-red-600 to-red-700 text-white font-bold py-4 px-8 rounded-xl hover:from-red-700 hover:to-red-800 transition-all duration-300 shadow-lg hover:shadow-xl transform hover:-translate-y-1 disabled:opacity-50 disabled:cursor-not-allowed"
            >
              <span v-if="!isLoading" class="flex items-center justify-center">
                <svg class="w-5 h-5 mr-2" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z" clip-rule="evenodd"></path>
                </svg>
                Lacak Sekarang
              </span>
              <span v-else class="flex items-center justify-center">
                <svg class="animate-spin -ml-1 mr-3 h-5 w-5 text-white" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
                  <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
                  <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
                </svg>
                Mencari...
              </span>
            </button>
          </form>

          <!-- Sample Tracking Result -->
          <div v-if="showSampleResult" class="mt-8 p-6 bg-gray-50 rounded-xl">
            <h3 class="font-semibold text-gray-900 mb-4 flex items-center">
              <svg class="w-5 h-5 text-green-500 mr-2" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
              </svg>
              Status Pengiriman
            </h3>

            <div class="space-y-4">
              <div class="flex items-center">
                <div class="w-4 h-4 bg-green-500 rounded-full mr-4"></div>
                <div>
                  <div class="font-medium text-gray-900">Paket Terkirim</div>
                  <div class="text-sm text-gray-600">25 Jan 2025, 14:30 WIB</div>
                  <div class="text-sm text-gray-600">Diterima oleh: Penerima</div>
                </div>
              </div>

              <div class="flex items-center">
                <div class="w-4 h-4 bg-blue-500 rounded-full mr-4"></div>
                <div>
                  <div class="font-medium text-gray-900">Dalam Perjalanan</div>
                  <div class="text-sm text-gray-600">25 Jan 2025, 08:00 WIB</div>
                  <div class="text-sm text-gray-600">Jakarta Pusat - Jakarta Selatan</div>
                </div>
              </div>

              <div class="flex items-center">
                <div class="w-4 h-4 bg-gray-400 rounded-full mr-4"></div>
                <div>
                  <div class="font-medium text-gray-900">Paket Diproses</div>
                  <div class="text-sm text-gray-600">24 Jan 2025, 20:15 WIB</div>
                  <div class="text-sm text-gray-600">Sortir Center Jakarta</div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Quick Actions -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mt-8">
          <a href="#" class="bg-white/10 backdrop-blur-sm text-white p-4 rounded-xl text-center hover:bg-white/20 transition-all duration-300">
            <svg class="w-8 h-8 mx-auto mb-2" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-7-4a1 1 0 11-2 0 1 1 0 012 0zM9 9a1 1 0 000 2v3a1 1 0 001 1h1a1 1 0 100-2v-3a1 1 0 00-1-1H9z" clip-rule="evenodd"></path>
            </svg>
            <div class="font-semibold">Komplain</div>
          </a>

          <a href="#" class="bg-white/10 backdrop-blur-sm text-white p-4 rounded-xl text-center hover:bg-white/20 transition-all duration-300">
            <svg class="w-8 h-8 mx-auto mb-2" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M3 4a1 1 0 011-1h4a1 1 0 010 2H6.414l2.293 2.293a1 1 0 01-1.414 1.414L5 6.414V8a1 1 0 01-2 0V4zm9 1a1 1 0 010-2h4a1 1 0 011 1v4a1 1 0 01-2 0V6.414l-2.293 2.293a1 1 0 11-1.414-1.414L13.586 5H12zm-9 7a1 1 0 012 0v1.586l2.293-2.293a1 1 0 111.414 1.414L6.414 15H8a1 1 0 010 2H4a1 1 0 01-1-1v-4zm13-1a1 1 0 011 1v4a1 1 0 01-1 1h-4a1 1 0 010-2h1.586l-2.293-2.293a1 1 0 111.414-1.414L15.586 13H14a1 1 0 01-1-1z" clip-rule="evenodd"></path>
            </svg>
            <div class="font-semibold">Ubah Alamat</div>
          </a>

          <a href="#" class="bg-white/10 backdrop-blur-sm text-white p-4 rounded-xl text-center hover:bg-white/20 transition-all duration-300">
            <svg class="w-8 h-8 mx-auto mb-2" fill="currentColor" viewBox="0 0 20 20">
              <path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"></path>
            </svg>
            <div class="font-semibold">Hubungi CS</div>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const trackingNumber = ref('')
const isLoading = ref(false)
const showSampleResult = ref(false)

const trackPackage = async () => {
  isLoading.value = true

  // Simulate API call
  setTimeout(() => {
    isLoading.value = false
    showSampleResult.value = true
  }, 2000)
}
</script>
