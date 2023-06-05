<script setup lang="ts">
// In this section, we use @vueuse/head. Check this for more detail
// https://github.com/vueuse/head
useHead({
  title: "Grouzy Blog",
  meta: [
    {
      name: "description",
      content: "Grouzy Blog",
    },
  ],
})
</script>

<template>
  <div class="min-h-100vh block relative pb-30 flex flex-col">
    <Navbar />
    <main>
      <router-view :key="$route.path" />
      <ToTopBtn />
    </main>
  </div>
</template>
