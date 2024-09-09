<script setup>
import { RouterView } from 'vue-router'
import Navigation from './components/TheNavigation.vue'
import Footer from './components/TheFooter.vue'
</script>

<template>
  <Navigation />
  <RouterView />
  <Footer />
</template>

<style scoped></style>
