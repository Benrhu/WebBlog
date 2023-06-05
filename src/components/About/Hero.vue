<script lang="ts">
export default {
  name: 'AboutHero'
}
</script>

<template>
  <div class="grid grid-cols-2 gap-4 relative dark:text-elucidator-50 custom-background">
    <div class="md_col-span-2 pt-22 md_pt-24 text-center md_text-left">
      <span class="fs-base medium-fs-large font-semibold">Grouzy is all about blockchain business solutions </span>
      <h1
        class="fs-8 medium-fs-2 font-bold leading-9 md_leading-tight mt-4 mb-10 md_mb-8 relative md_w-auto mx-auto z-20 w-[350px]"
      >
        We develop the 
      </h1>
      <form action="/signup" method="get">
        <input
          class="flex mx-auto fs-large text-white bg-transparent border border-white border-opacity-20 rounded-full px-7 outline-none w-full md_w-[352px] h-[58px]"
          type="text"
          name="email"
          placeholder="Work e-mail..."
        /><input type="hidden" name="signup" value="index" />
        <button
          class="flex mx-auto justify-center pt-4 fs-large border w-50 font-semibold rounded-full bg-secondary-gradient mt-3-5 md_ml-3-5 md_mt-0 w-full md_w-[252px] h-[58px]"
        >
          Create Free Account!
        </button>
      </form>
    </div>
    <div class="md_col-span-2 pt-22 md_pt-24 md_text-left">
      <span class="fs-base medium-fs-large font-semibold">Chains. Data. Growth</span>
      <h1
        class="fs-8 medium-fs-2 font-bold leading-9 md_leading-tight mt-4 mb-10 md_mb-8 relative md_w-auto mx-auto z-20 w-[350px]"
      >
        Blockchain service to incentivize, reward and track employee behaviors
      </h1>
      <form action="/signup" method="get">
        <input
          class="flex mx-auto fs-large text-white bg-transparent border border-white border-opacity-20 rounded-full px-7 outline-none w-full md_w-[352px] h-[58px]"
          type="text"
          name="email"
          placeholder="Work e-mail..."
        /><input type="hidden" name="signup" value="index" />
        <button
          class="flex mx-auto justify-center pt-4 fs-large border w-50 font-semibold rounded-full bg-secondary-gradient mt-3-5 md_ml-3-5 md_mt-0 w-full md_w-[252px] h-[58px]"
        >
          Create Free Account!
        </button>
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
  border-radius: 50px;
  color: white;
  width: auto;
  height: 500px;
  margin: 0;
  background-size: 200% 200%;
  background-image: linear-gradient(45deg, black, #0000ff, #ff00ff);
  animation: gradient 5s infinite;
}

.custom-background input {
  background-color: white;

  width: 50%;
}

@keyframes gradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}
</style>
