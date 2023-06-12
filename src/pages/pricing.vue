<script setup lang="ts">
import Pricing from '../components/Services/PricingPerUser.vue'
</script>

<template>
  <div
    class="container mx-auto flex flex-wrap items-center text-elucidator-700 dark:text-dark-repulser-400 font-bold justify-center mt-16"
  >
    <h1 class="mb-16 text-3xl">Choose the size of your company</h1>
    <Pricing />
  </div>
</template>

<style scoped>
.container {
  max-width: 80rem;
}
</style>
