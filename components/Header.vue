<template>
  <header
    class="min-h-screen font-[Barlow] flex flex-col items-center justify-center text-center bg-white relative overflow-hidden"
  >
    <div class="absolute top-8">
      <!-- Ubicación y correo -->
      <div
        class="text-xs md:text-sm font-bold text-gray-800 top-1 tracking-wide mb-1"
      >
        IBAGUÉ, COLOMBIA
      </div>
      <div class="text-[10px] md:text-xs text-gray-400 mb-6">
        MILEERDUBANLEON@GMAIL.COM
      </div>

      <!-- Nombre principal -->
      <h1
        class="text-4xl md:text-7xl transform scale-y-110 font-bold text-[#333] mb-12 md:mt-0 mt-52"
      >
        MILEER LEÓN
      </h1>
    </div>

    <Gallery />

    <!-- Subtítulo -->
    <h2
      class="text-4xl md:text-9xl font-extrabold text-gray-300 mt-16 mb-4"
    >
      DESARROLLADOR
    </h2>

    <div class="absolute bottom-10">
      <!-- Clientes -->
      <p class="text-xs md:text-sm font-semibold text-gray-600 tracking-widest mt-4">
        CLIENTES
      </p>
      <p class="text-[10px] md:text-xs text-gray-400 mt-1">
        ALUMART Panamá, Garrafeira Canhoto, Maquinitas Guadalajara
      </p>
    </div>

    <!-- Ícono flotante superior derecho -->
    <div class="absolute top-4 right-4">
      <img src="" alt="Logo" class="w-6 h-6 md:w-8 md:h-8 rounded-full shadow-md" />
    </div>

    <!-- Ícono flotante inferior derecho -->
    <div class="absolute bottom-4 right-4">
      <img src="" alt="Palette" class="w-6 h-6 md:w-8 md:h-8" />
    </div>
  </header>
</template>

<script setup>
import Gallery from '@/components/Gallery.vue'
</script>
