<template>
  <div
    class="fixed bottom-6 left-6 z-40
           px-4 py-2
           rounded-full
           bg-white/80 backdrop-blur
           shadow-md
           border border-black/5
           text-xs text-gray-700
           flex items-center gap-2"
  >
    <!-- Icono -->
    <svg
      xmlns="http://www.w3.org/2000/svg"
      class="w-4 h-4"
      fill="none"
      viewBox="0 0 24 24"
      stroke="currentColor"
      stroke-width="2"
    >
      <path
        stroke-linecap="round"
        stroke-linejoin="round"
        d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"
      />
      <path
        stroke-linecap="round"
        stroke-linejoin="round"
        d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"
      />
    </svg>

    <span>
      {{ visits }} visitas
    </span>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const visits = ref(0)

// ⚠️ Cambia esto por algo único (tu dominio o nombre)
const NAMESPACE = 'mileer-portfolio'
const KEY = 'home-visits'

onMounted(async () => {
  try {
    const res = await fetch(
      `https://api.counterapi.dev/v2/mileer-leons-team-2443/first-counter-2443`
    )
    const data = await res.json()
    visits.value = data.value
  } catch (e) {
    console.error('No se pudo obtener el contador')
  }
})
</script>
