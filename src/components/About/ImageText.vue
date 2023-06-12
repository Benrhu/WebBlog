<script setup lang="ts">
import { ref } from "vue"
import solution from '../../assets/images/solution.png'
import team from '../../assets/images/team2.png'
import remote from '../../assets/images/remote.png'

const features = ref([
  {
    name: "Remote team",
    description:
      "We love to provide flexibility, both in terms of time and organization, with the aim of helping to reconcile personal and professional life.",
    image: remote,
  },
  {
    name: "Talented people",
    description:
      "We focus on looking for experienced minds, eager to learn and above all, with a passion for blockchain.",
    image: team,
  },
  {
    name: "We solve problems",
    description: "Every person in Grouzy loves solving problems and is eager to hear yours.",
    image: solution,
  },
])
</script>

<template>
  <div class="container mx-auto">
    <h1
          class="fs-8 medium-fs-2 text-3xl leading-9 md_leading-tight mt-4 mb-10 md_mb-8 relative md_w-auto mx-auto z-20 w-full text-center dark:text-white"
        >
          Our 3 pillars
        </h1>
    <div class="features-container grid-cols-3">
      <div
        v-for="(feature, index) in features"
        :key="index"
        class="feature-card dark:text-black"
      >
        <img class="w-100 p-10" :src="feature.image" alt="" srcset="" />
        <p class="feature-name">{{ feature.name }}</p>
        <p class="feature-description">{{ feature.description }}</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.features-container {
  margin-top: 10px;
  display: grid;
  justify-content: space-around;
  flex-wrap: wrap;
}
.feature-card {
  background-color: white;
  border-radius: 10px;
  padding: 20px;
  margin: 30px;
  width: 400px;
  text-align: center;
}
.feature-name {
  font-size: 1.25rem;
  font-weight: 500;
  margin-bottom: 10px;
  text-align: center;
}
.feature-description {
  font-size: 16px;
  margin-bottom: 10px;
}
.shadow {
  box-shadow: rgba(149, 157, 165, 0.2) 1px 18px 44px 10px;
}

.skyblue {
  color: #3400ff;
}

.container {
  max-width: 80 rem;
}
</style>
