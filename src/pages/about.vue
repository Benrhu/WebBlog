<script setup lang="ts">
import Features from "~/components/About/Features.vue"
import AboutHero from '~/components/About/Hero.vue'
import AboutUs from '~/components/About/AbutUs.vue'
import ImageText from '~/components/About/ImageText.vue'
</script>

<template>
  <div class="container mx-auto">
    <AboutHero />
    <AboutUs />
    <ImageText />
  </div>
</template>

<style scoped>
.container {
  max-width: 80rem;
}
</style>
