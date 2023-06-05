<script setup lang="ts">
import Features from "~/components/About/Features.vue"
import AboutHero from '~/components/About/Hero.vue'
</script>

<template>
  <div class="container mx-auto">
    <AboutHero />
    <Features />
  </div>
</template>

<style scoped>
.container {
  max-width: 80rem;
}
</style>
