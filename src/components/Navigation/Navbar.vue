<script setup lang="ts">
import { isDark, toggleDark, slug } from "~/utils"
import type { NavbarMenu } from "~/types"

// https://vueuse.org/shared/useToggle/
const [search, setSearch] = useToggle()
const [open, setOpen] = useToggle()

// https://vueuse.org/core/onKeyStroke/
onKeyStroke("Escape", () => {
  search.value = false
})
onKeyStroke("Escape", () => {
  open.value = false
})

// https://vueuse.org/core/onClickOutside/
const modalSearch = ref(null)
onClickOutside(modalSearch, (e) => {
  search.value = false
})

const navbottom = ref(null)
onClickOutside(navbottom, (e) => {
  open.value = false
})

const router = useRouter()

// Hide navbottom after page has been changed
router.afterEach(() => {
  open.value = false
})

// Navbar list
const dataNavbar: NavbarMenu[] = [
  {
    name: "Home",
    to: "/",
  },
  {
    name: "Pricing",
    to: "/pricing",
  },
  {
    name: "Blog",
    to: "/blog",
  },
  {
    name: "About",
    to: "/about",
  },
]
</script>

<template>
  <nav
    class="text-elucidator-700 dark:text-dark-repulser-400 h-20"
    role="navigation"
    aria-label="navbar"
  >
    <div class="max-w-screen-xl mx-auto h-full flex flex-row items-center space-x-60">
      <div class="">
        <router-link to="/" class="font-bold text-2xl">
          <img
            class="w-50"
            src="../../assets/images/grouzy_logo-transparent.png"
            alt=""
            srcset=""
          />
        </router-link>
      </div>
      <div class="flex flex-wrap items-center">
        <router-link
          v-for="(data, i) in dataNavbar"
          :key="i"
          class="mr-5 py-1.5 px-3 rounded-md text-elucidator-700 dark:text-dark-repulser-400 dark:hover:text-elucidator-300 hover:text-gray-900 hidden lg:block"
          :to="data.to"
          active-class="bg-gray-200 dark:bg-gray-500 dark:text-dark-repulser-200"
          >{{ data.name }}</router-link
        >
      </div>
      <carbon-sun
        v-if="isDark"
        class="mr-5 cursor-pointer text-elucidator-700 dark:text-dark-repulser-400"
        tabindex="0"
        @click="toggleDark"
        title="Toggle light mode"
      />
      <carbon-moon
        v-else
        class="mr-5 cursor-pointer text-elucidator-700 dark:text-dark-repulser-400"
        tabindex="0"
        @click="toggleDark"
        title="Toggle dark mode"
      />
    </div>
  </nav>
</template>

<style lang="scss">
.active-class {
  @apply p-2 mb-2 rounded-md bg-elucidator-200 dark:bg-elucidator-700;
}

.hover-skyblue:hover {
  background-color: skyblue;
}

.container {
  max-width: 80rem;
}

.custom-flex {
  -webkit-box-flex: 1;
  -ms-flex: 1 1 0%;
  -webkit-flex: 1 1 0%;
  flex: 1 1 0%;
}
</style>
