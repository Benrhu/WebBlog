<script lang="ts"></script>

<template>
  <div class="grid grid-cols-3 gap-4 relative dark:text-elucidator-50 custom-background">
    <div class="col-span-full md_col-span-2 pt-12 md_pt-24 text-center md_text-left">
      <span class="fs-base medium-fs-large font-semibold">Chains. Data. Growth</span>
      <h1
        class="fs-8 medium-fs-2 font-bold leading-9 md_leading-tight mt-4 mb-10 md_mb-8 relative md_w-auto mx-auto z-20 w-[350px]"
      >
        Blockchain service to incentivize, reward and track employee behaviors
      </h1>
      <form class="container mx-auto pt-5" action="/signup" method="get">
        <input
          class="flex mx-auto fs-large text-white bg-transparent border border-white border-opacity-20 rounded-full px-7 outline-none w-full md_w-[350px] h-[58px]"
          type="text"
          name="email"
          placeholder="Work e-mail..."
        /><input type="hidden" name="signup" value="index" />
        <router-link to="" class="font-bold">
          <button
            class="flex mx-auto justify-center pt-4 fs-large border w-50 font-semibold rounded-full bg-secondary-gradient mt-3-5 md_ml-3-5 md_mt-0 w-full md_w-[252px] h-[58px]"
          >
            Create Free Account!
          </button>
        </router-link>
      </form>
    </div>
  </div>
</template>

<style scoped>
@keyframes float {
  0% {
    transform: translatey(0px);
  }
  50% {
    transform: translatey(-20px);
  }
  100% {
    transform: translatey(0px);
  }
}
.float {
  animation: float 3s ease-in-out;
}

.custom-background {
  color: white;
  width: auto;
  height: 50vh;
  margin: 0;
  background-size: 100%;
  background-image: url("../../assets/images/hero.png");
}

.custom-background input {
  background-color: white;
  width: 50%;
}

.container {
  max-width: 80rem;
}
</style>
