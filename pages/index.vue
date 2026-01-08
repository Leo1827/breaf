<template>
  <div class="min-h-screen flex flex-col">
    <Header />
    <ProjectFloating />
    <ProjectFloatingVercel />
    <Footer />
    <ThemeToggle />
  </div>
</template>

<script setup>
import Header from '@/components/Header.vue'
import ProjectFloating from '@/components/ProjectFloating.vue'
import ProjectFloatingVercel from '@/components/ProjectFloatingVercel.vue'
import Footer from '@/components/Footer.vue'
import ThemeToggle from '@/components/ThemeToggle.vue'
</script>
