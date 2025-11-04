<template>
  <div class="min-h-screen flex flex-col">
    <Header />
    <ProjectFloating />
    <ProjectFloatingVercel />
    <Footer />
  </div>
</template>

<script setup>
import Header from '@/components/Header.vue'
import ProjectFloating from '@/components/ProjectFloating.vue'
import ProjectFloatingVercel from '@/components/ProjectFloatingVercel.vue'
import Footer from '@/components/Footer.vue'
</script>
