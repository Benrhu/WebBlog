<script setup lang="ts">
import { ref } from "vue"

const features = ref([
  {
    name: "Blockchain DNA",
    description:
      "We are so aware of the potential and benefits of the blockchain that we are willing to give up our lives to ensure that everyone can enjoy its benefits. For this reason, we are committed to improving the blockchain industry.",
    description1: "For this reason, we are committed to improving the blockchain industry.",
    icon: "path/to/icon1.png",
  },
  {
    name: "We solve problems",
    description:
      "We love to rack our brains to create solutions that fit perfectly with the needs to be solved. We feel like 007 agents with the latest technology on the market, but instead of blowing up, we grow companies.",
    description1:
      "We feel like 007 agents with the latest technology on the market, but instead of blowing up, we grow companies.",
    icon: "path/to/icon2.png",
  },
  {
    name: "We help freelancers",
    description: "We want to promote the use and growth of blockchain professionals.",
    description1:
      "For this reason, we also provide free and paid training and resources for those who want to work as blockchain professionals.",
    icon: "path/to/icon2.png",
  },
  {
    name: "100% flexibility",
    description:
      "The good thing about having dna blockchain, is that we can adapt to 100% of the needs and tastes of our customers.",
    description1:
      "The Blockchain is like a kind of technological plasticine that you can mold to your liking to solve and improve your company.",
    icon: "path/to/icon2.png",
  },
])
</script>

<template>
  <div class="features-container">
    <div
      v-for="(feature, index) in features"
      :key="index"
      class="feature-card shadow dark:text-white"
    >
      <h2 class="feature-name">{{ feature.name }}</h2>
      <p class="feature-description">{{ feature.description }}</p>
      <p class="feature-description">{{ feature.description1 }}</p>
    </div>
  </div>
</template>

<style scoped>
.features-container {
  margin-top: 100px;
  display: flex;
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

.feature-card:hover {
  background-image: linear-gradient(45deg, gray, white, gray);
  animation: gradient 3s;
  background-size: 200% 200%;
}

@keyframes gradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 0%;
  }
}

.feature-name {
  font-size: 20px;
  font-weight: bold;
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
</style>
