<script setup lang="ts">
import { ref } from "vue"
import certificate_2 from '../../assets/images/certificate_2.png'
import rules from '../../assets/images/10492.jpg'
import on_chain from '../../assets/images/on_chain-removebg-preview.png'

const features = ref([
  {
    name: "1. Decide the rules",
    description:
      "Create rules to establish how employees are rewarded in your company based on the behaviors they engage in.",
    image: rules,
  },
  {
    name: "2. Our system rewards",
    description:
      "Our system detects the behaviors of your employees and according to the established rules, rewards or penalizes.",
    image: on_chain,
  },
  {
    name: "3. Enjoy the tokens",
    description: "Every person who is registered as an employee, from the cleaning staff to the c-levels, is rewarded based on their behavior.",
    image: certificate_2,
  },
])
</script>

<template>
  <div class="container mx-auto">
    <div class="col-span-full md_col-span-2 pt-12 md_pt-24 text-center md_text-left dark:text-white">
      <h1
        class="fs-8 medium-fs-2 text-3xl leading-9 md_leading-tight mt-4 mb-10 md_mb-8 relative md_w-auto mx-auto z-20 w-full"
      >
        Improve your business performance
      </h1>
      <h2>Reward your employees as they deserve and become a model company.</h2>
      <p class="w-70vh mx-auto mt-9">
        Rewards or penalizes behaviors such as delivering a project early, helping another
        department even if it is not your role, contributing ideas or harassing other co-workers.
      </p>
    </div>
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
