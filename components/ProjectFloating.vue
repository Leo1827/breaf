<template>
  <section
    class="relative w-full min-h-screen flex flex-wrap justify-center items-center gap-6 bg-white overflow-hidden font-[Barlow]"
  >
    <!-- Fondo con animación sutil -->
    <div class="absolute inset-0 bg-gradient-to-br from-gray-50 to-white animate-pulse-slow opacity-50"></div>

    <div
      v-for="(project, index) in projects"
      :key="index"
      class="group relative w-64 h-80 bg-white rounded-2xl shadow-lg hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-3 hover:rotate-2"
      :style="getFloatingStyle(index)"
    >
      <div class="absolute inset-0 bg-gradient-to-t from-gray-100/60 via-gray-300/20 to-transparent rounded-2xl"></div>

      <img
        :src="project.image"
        :alt="project.title"
        class="w-full h-1/2 object-cover rounded-t-2xl"
      />

      <div class="p-4 text-left relative z-10">
        <h3 class="text-lg font-bold text-gray-800 mb-1">
          {{ project.title }}
        </h3>
        <p class="text-xs text-gray-500 mb-3">{{ project.tech }}</p>
        <p class="text-sm text-gray-600 leading-snug line-clamp-3">
          {{ project.description }}
        </p>
      </div>

      <div class="absolute bottom-1 left-4">
        <a
          :href="project.link"
          target="_blank"
          class="text-[10px] font-semibold tracking-wider text-gray-800 group-hover:text-blue-500 transition"
        >
          VER PROYECTO →
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

// Lista de proyectos (puedes reemplazar las imágenes y links)
const projects = ref([
  {
    title: 'Canhoto Premium',
    tech: 'Laravel • Tailwind • JS • MySQL',
    description:
      'Tienda online con acceso a subscripción, vinos exclusivos, facturación, inventario, panel administrador, responsive.',
    image: '/images/1111.PNG',
    link: 'https://canhotopremium.com/'
  },
  {
    title: 'Canhoto Black',
    tech: 'PHP • HTML • Tailwind • JS',
    description:
      'Landing page, formularios con Mailer y manejo de rendimiento con pixie Facebook.',
    image: '/images/22.PNG',
    link: 'https://www.canhotoblack.com/'
  },

])

// Genera posiciones flotantes aleatorias para simular movimiento
const getFloatingStyle = (index) => {
  const offset = (index % 2 === 0 ? 1 : -1) * (5 + index * 2)
  const animation = `float-${index % 3}`
  return {
    animation: `${animation} 6s ease-in-out infinite`,
    transform: `translateY(${offset}px)`
  }
}
</script>

<style scoped>
@keyframes float-0 {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
}
@keyframes float-1 {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(8px); }
}
@keyframes float-2 {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-12px); }
}

/* Animación de fondo sutil */
@keyframes pulse-slow {
  0%, 100% { opacity: 0.5; }
  50% { opacity: 0.8; }
}
</style>
